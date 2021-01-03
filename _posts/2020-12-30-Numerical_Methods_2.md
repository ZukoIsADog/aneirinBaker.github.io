---
layout: posts
title: Numerical Methods 2 - Higher Order Methods
tags: [Numerical Methods, ODE, Python]
tagline: ""
header:
  overlay_image: /assets/img/unsplash-image-1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---

Previously we discussed how to solve some simple ODE's and looked at coding a simple Euler algorithm. However wr found that the solution we used doesn't always work. This will be a feature of these posts, finding solutions to where our current methods fail. 

To understand why the Euler method failed we must first understand where it comes from. I mentioned in the previous post that it comes from a discretsation which is a simple enough explanation but hides quite alot. 

When we discretise a system we naturally are throwing away some of the intformation in that system. There is a vast literature on this so i will only be brief in my explanation and point the interest reader to wards some more extensive reviews of the topic. 

Discretization comes from the taylor expansion of the function itslef.

\\[ f(x) = \frac{f(0)}{0!} + \frac{f'(0) x}{1!} + \frac{f'' (0) x^2}{2!} + ...\\]

If we truncate this to second order in \\[x\\] then we find the definition of the deritive from the previous post. However ther are many more tems in this series to take account of. This is the main problem, when these terms become large then we can no longer discount them. If we do (as we did in the Euler method) we are punished and the solution our method produces can be vastly diffrent from the true solution

To account for this the most obvious thing to do is to include more terms. These types of methods are called higher order methods and are one of the ways we can improve the accuracy of our algorithms. 

This inlcusion of higher order terms from the Taylor expansion leads to a family of methods known as the Runge-Kutta methods. These include one of the most used methods for solving ODE's the 4th order Runge-Kutta (or RK4 for short). There are lots of other methods for solving ODE's but i do not want to dwell on them too much so i shall leave a link to some of them for anyone who wants to look into them more. 

Here i shall look at the derivation of the second and fourth order Runge-Kutta method and compare the two. 

We concider the first-order ODE system.

\\[ \frac{dy}{dt} = f(t,y(t)) \\]

Since we want a second order method we should start with the Taylor exoanion of a function

\\[ y(t+h) = y(t) + h y'(t) + \frac{h^2}{2} y'' (t) + O (h^3)\\]

We an replace the first order deritive with teh RHS of our ODE system, we can also replace the second order deritive with a chain rule expansion

\\[ \frac{d^2y}{dt^2} = \frac{df}{dt} + \frac{df}{dy} \frac{dy}{dt}\\]

The Taylor expansion becomes 

\\[  y(t+h) = y(t) + h f(t,y) + \frac{h^2}{2} [\frac{df}{dt} + \frac{df}{dy} \frac{dy}{dt}] \\]
***** check what goes on here not sure about it****
 
 We now recall the taylor expansion for a multi varied function 

\\[  f(t+h, y+k) = f(t,y) + h \frac{\partial f}{\partial t} + k \frac{\partial f}{\partial y} + ... \\]

Thus we can interpret the term in brackets as a multivaried taylor expansion, thus getting the following 

\\[ y(t+h)  = y(t) + \frac{h}{2} f(t,y) + \frac{h}{2} f(t+h,y+h f(t,y)) + O(h^3)\\] 

Translating this quickly into a numerical method we have 

\\[ y_{n+1} = y_n + \frac{h}{2}(k_1 + k_2)  \\]

where

\\[ k_1 = f(t_n,y_n) \quad \text{and} \quad k_2 = f(t_n + h , y_n + h k_1 )\\]

This is the classical second-order Runge-Kutta method. It is also known as Heun’s method or the improved Euler method.

We can compare this to the Euler method to see how much better this is. 


ALSO NOTE ABOUT THE FAMILT OF METHODS WHICH CAN BE DERIVED.

************** code comparison goes here ********************

##Runge Kutta fourth ORder

The work house of most Differential equation solver such as ode45 in matlab and scipy's RK45 both of which implement the RK4/5 algorithm to solve differential equations. The RK4 method is 

\\[ y_{n+1} = y_n  + \frac{1}{6} (k_1 + k_2 + k_3 + k_4)\\]
with 
\\[k_1 = f(t_n, y_n)\\]  
\\[k_2 = f(t_n + \frac{h}{2}, y_n + h \frac{k_1}{2})\\]  
\\[k_3 = f(t_n + \frac{h}{2}, y_n + h \frac{k_2}{2})\\]  
\\[k_4 = f(t_n + h, y_n + h k_3)\\]  

 ************** code example goes here ********************


 Now that we have looked at some higher order methods we shall turn to a subject not quite as exciting but non the less important. We shall examine Error analysis and stability of these algorithms as it will be important to concider these concepts when we look at algorithms in the future.


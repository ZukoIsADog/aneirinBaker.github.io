---
layout: posts
title: Numerical Methods 2 - Higher Order Methods and Stability
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

If we truncate this to second order in \\[x\\] then we find the definition of the deritive in the previous post
---
layout: posts
title: Quantum Computing 2 - A Bog Standard Introdution to Quantum Computing
tags: [Quantum Computing]
tagline: ""
header:
  overlay_image: /assets/img/General/unsplash-image-1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---


## A Bog Standard Introdution to Quantum Computing
As with most introductions to scientific books and blogs there always has to be sections that are repeated everywhere. Since quantum computing has been hot in the media for a while there have been many many blog posts on quantum computing, what it entails and its challenges. Here i may repeat all of this but i am doing it for completion bascially it needs to be done. I shall go over the basic make up of a quantum computer (qubits),what you can do with this qubits and most importantly why they differ from classical qubits. 

### Clascial Bits

To understand qubits and the difference from your laptop/desktop/phone to a quatum computer first you must understand what the basic compent of classical computer is. The bit or logical bit is a system that can only take two values (1 or 0, on or off, left or right etc). Using this and basic logical operations such as (XOR, NOT etc) all possible algoirhtms can be approximated using these (....cit turing thesis?). An example of an adder 


<p><img src="https://upload.wikimedia.org/wikipedia/commons/9/92/Halfadder.gif" alt="Halfadder.gif">
<figcaption><a href="https://commons.wikimedia.org/wiki/File:Halfadder.gif">Marble machine</a>, <a href="https://creativecommons.org/licenses/by-sa/4.0">CC BY-SA 4.0</a>, via Wikimedia Commons</figcaption>
</p>



### Qubits 

Qubits are the quantum mechanial extension of the classical bit they are infinite level systems however only the lowest two levels (in most cases) are allowed to be accessed making them effectivly a two level system (a bit). The difference over classcila bits is the possibility of what is know as superposition (and it's extension to multiple qubit called entanglement). This property allows the different states to "mix" and become part one state and part another state. We represent this state in Dirac notation (link)

<head>
  <script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
  <script id="MathJax-script" async
          src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
  </script>
</head>

<body>
<p>
  \[ |0> \quad \text{and} \quad  |1>\]

You may notice that these two states are put into odd looking bracket notation, this is called dirac notation. It represents a vector in an infiite dimensional hilbert space ( If you don't know what any of those mean i will leave a link to a video my friend has made on Quantum Mechanics.) for our purposes though we will not need to worry about the maths behind this notation but only worry about the fact that these represent two ditinct states. The full state of our system is then given by 
\[ | \psi > =   N(\alpha_0 |0> + \alpha_1 |1> )\]
Where the factor of N in the front ensures that the state is properly normalised so we get probabilities we can interpret at the end. By normalization we mean that \( < \psi| \psi > = 1  = | \alpha_0|^2 + | \alpha_1 |^2 \), this normlaization ensures that the states in quantum mechanics are unit vectors. We can also represent these states as vectors 
\[ 
  | \psi > =\begin{pmatrix}
           		\alpha_0 \\
           		\alpha_1 \\
         	\end{pmatrix}
\]

</p>
</body>

### Types of Quantum Computer


There are several types of quantum computer currently in development the most popular one is a gate based mechanics, it works very much like a clasical computer using different types of quantum logic gates to perform calculations. Perhaps the second most popular type is a quantum annelaer, these are the computers produced by the canadian company D-Wave. They do not use gates but rather they evelove their system forward in time until the system slowly changing from one known system to another (unknown) system to extract information from it. I shall make a post later about this system as the exact way that this is performed is quite interesting. The last type of quantum computer is called a quantum simulator, it is very similar to a quantum annealer however it is even more specific. A quantum simulator is a quantum system that has been tuned to simulate another quantum system, this may sound weird but in experiemtnal physics it is often very hard to control certain phenomena. Thus if we can tune a easily controllable phenomena to look like another we can make measurements on that system to learn about the complucated system.  

For now we shall focus on gate based quantum computers as they are the most common and perhaps the most fleshed our type of QC especially as several large companies have a gate baed QC in development (IBM,Google and Rigetti).



### Quantum Gates

In what is known as the gate based model of quantum computing quantum gates are the central driving force of this mode of operation. They are genrally split up by the number of qubits they act on and the more qubits you wish to act on the more complited the gate and thus the harder the implementation. Larger gates also tend to take longer and aften broken down into a series of lower order gates. 

#### Single Qubite

In general quantum gates are resresented much like clasical logic gates below you can see some example of one qubit gates and their matrix representation.

<figure>
  <img src="/assets/img/QC2/QuantumGates.png" alt="QuantumGates" height="50"/>
</figure>

The lines or wires in the above image represents a qubit or the state of a qubit and the boxes are the transformations that occur. As an example we shall focus on the Pauli-X gate which is also called the "bit-flip" gate since its action on a qubit is to flip the state from a \( |0> \) state to a \( |1> \) state. It's matrix representation is given by 

<body>
<p>
\[ 
  X =\begin{pmatrix}
           		0 & 1\\
           		1 & 0 
         	\end{pmatrix}
\]

We can also ask what this matrix does to a superposition state well lets take the most basic superposition state we can think of \( \frac{1}{\sqrt{2}} (|0> + |1>)\) and apply the X gate to this. We shall find that we get the same output state. If you have done any linear algebra to university level you will know that this is what is known as an eigen vector of this matrix. There is another one it is \( \frac{1}{\sqrt{2}} (|0> - |1>)\), it may not look like an eigne vector but that is becuase when the X gate is applied to this it will pick up a phase factor of -1. Now you may ask how on earth could we create these superposition states. Well we can create a gate to do these, infact there is a very famous gate that produces these very eigenstates, it is called the Hadamard Gate. It's matrix representation is 

\[ 
  H =\begin{pmatrix}
           		1 & 1\\
           		1 & -1 
         	\end{pmatrix}
\]
If we apply this to the \( |0> \) and  \( |1> \) state you will find the superposition states that we mentioned above pop out.
</p>
<p>
	There are many other gates you can perfrom in Quantum Computer, a reasonably exhaustive list can be found on wikipieadia (link below) but for now these two shall suffice as an introduction. 
</p>
</body>

#### Two Qubit Gates

<body>
<p>
Two qubit gates do what it says on the tin, they act on two qubits to produce a result that a single qubit gate could not. It may not seem like it but we are now truly moving into a purely quantum realm. Why? This is because we are now discussing operations which cannot be perforomed with clasial logic bits. Now there are severl single qubit gates which obviously cannot be performed with clasical bits but thats more to do with the acutal qubits themselves rather than the make up of the logic. The first two qubit gate that is always discussed is the Controlled Not gate or CNOT gate. A quick and dirty explanation of this gate is that it flips a target qubit dependant on the state of a control qubit. Its matrix representation is given by
</p>

\[
\begin{pmatrix} 
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\ 
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0 
 \end{pmatrix} 
\]
</body>
The reason this gate is so important is that when combined with the Hadamard and two other single qubit gates creates what is known as a universal quantuma gate set. Meaning that with this gate set we can approximate any quantum algorithm to within an arbitary error. This roughly translates to we can perfrom any quantum algorithm you can come up with. This is great so why is there anything else? Why don't we stop here. 



#### Multi Qubit Gates

The Questions posed just above are very relavent. Why is there still research into higher order interactions if we can perfrom all algorithms with what we have. Well the answer is that even though we CAN perforom all algorithms doesn't mean that it is effiecnt to. A prime example (one from my PhD) is the Toffoli gate. This gate when decomposed requires at least 5 CNOT gates and many other single qubit gates. Now whilst individially these gates are very fast when you are combining many of them together it starts to get alot slower. In the case of the Toffoli gate you approach the coherence time of the qubits you are using (if using superconduting circuits) or it just becomes ineffecint to perform this gate (in the case of Trapped Ions where the gate times are much slower). 



### Links and References

https://en.wikipedia.org/wiki/Quantum_logic_gate


<a href="https://www.mathjax.org">
    <img title="Powered by MathJax"
    src="https://www.mathjax.org/badge/badge.gif"
    border="0" alt="Powered by MathJax" />
</a>
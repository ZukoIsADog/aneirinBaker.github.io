---
layout: posts
title: Quantum Computing Hackathon 2022
subtitle: 
tags: [Quantum Computing, Code]
tagline: ""
header:
  overlay_image: assets/img/General/unsplash-image-1.jpg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---

# First Quantum Computing Hackathon

At the tail end of the heatwave of 2022 I was invited down to Royal Holloway London to take part in the first Quantum Hackathon organized by the National Quantum Computing Center. We were split into teams and assigned a company for which we would explore the applications of quantum computing to their industry. I was assigned to MBDA systems and we set out to explore how we can apply quantum computing to Monte Carlo Tree Search which is a method that is used in artificial intelligence systems related to playing games. It has been used in some of the earlier versions of the systems that were used to play games. In short the system takes the current state of the system and plays out the game randomly remembering which moved resulted in a win or loss. This memory informs the exploration and eventually it ends up with a set of moves it thinks is likely to win the game. In current implementations the games are played classically using an almost brute force method. A better way and a way in which the second generation of these AI's used is to learn the game using some reinforced learning techniques. We choose to examine the improvements that Quantum computing could give to this system. 

Before we can examine how exactly we wish to involve quantum computing in this we need to describe the game we choose to play. This is a well known game in the Game theory community, the game is played on a grid or lattice that contains a monster and a princess. The monster wishes to catch the princess, the princess can move in any way (static, random, directed etc) and the idea of our system is that the monster will learn the best way to catch the princess. This was done via reinforcement learning however in place of one of the classical layers we switched out a quantum layer.

<p align="center">
  <img width="460" height="300" src="/assets/img/hackathon/NN.png">
</p>

We implemented the system using a combination of machine learning packages such as gym to create the. Then we added in a quantum computing layer using qiskits machine learning package. The game we created was coded ourselves and you can see some nice gifs of the monster catching the princess below with random movement. 

<p align="center">
  <img width="460" height="300" src="/assets/img/hackathon/10_node_game.gif">
</p>

With the machine learning code and the game we wish to lean set up we began by training the system using qiskits in built quantum simulators, we only used three qubits for our quantum layer as the circuit gets big really fast (see below)

<p align="center">
  <img width="460" height="300" src="/assets/img/hackathon/circuit.png">
</p>

Training this system over night we found some improvements over the classically trained model. However it must be noted that the classical training is significantly quicker than the quantum training. Some improvement can probably be found in optimizing the circuit and maybe using a better simulator (and hardware.....our poor laptops). But we did manage to find some improvements using the quantum system over the classical system, why this is and whether it is significant is a question which would probably take more than two pizza fueled days to answer but none the less it's an improvement. We can however argue that there will be improvement in computation time when used on a real quantum computer since the number of possible state grows exponentially on a Quantum Computer thus a register of 15 qubits is the same as a layer with ~30000 nodes - this obviously comes with all the usual caveats of fidelity, gate time etc. 
I must also add that running the quantum layer on IBMs manila quantum computer resulted in nothing more than noise for each run, mainly due to the depth of the circuit being ~100 and containing many CNOT gates whose fidelity (even on this small machine) is only ~90%.

Putting aside the shaky ground that our results are on it was a really fun experience to create this in just two short days, I loved doing this in the team I was with and am looking forward to next years hackathon :D 

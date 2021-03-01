---
layout: posts
title: Quantum Computing 1 - Introduction to Quantum Computing Architectures
tags: [Quantum Computing]
tagline: ""
header:
  overlay_image: /assets/img/General/Quantum_Banner.jpeg
  overlay_filter: 0.5 # same as adding an opacity of 0.5 to a black background
  caption: "Photo credit: [**Unsplash**](https://unsplash.com)"
---

Quantum Computing is posed to become one of the most useful technologies invented. It boasts algorithms that can outperform some of the best classical algorithms in areas such as root finding and Database searching. These may sound mundane however they could have huge applications to the technology world if they are achieved. 

In this series of blog posts I will explore how Quantum Computers work, what algorithms can be executed on them and how much improvement we can expect from these algorithms.

We begin with an exploration of the proposed architectures for Quantum Computers. There are Two main contenders and several other interesting ones which are less developed. 

### Superconducting Circuits  
<figure>
  <img src="/assets/img/QC1/Google_Quantum_Nature.png" alt="Trulli" style="height:80%">
  <figcaption>Google's Sycamore Quantum Computer</figcaption>
</figure>
Superconducting circuits are artificial atoms based on superconducting wires and nonlinear elements. They have to be cooled to very low temperatures (~10mK) so their superconducting nature can appears. When these circuits are superconducting they act like nonlinear oscillators ( due to a nonlinear element called a Josephson junction), using this nonlinearity we can isolate the bottom two energy levels to create a qubit (almost) or two level system. These systems are some of the most advanced architectures of quantum computers to date. The largest Quantum computer (Google's sycamore) was made using SCC's and had 50 (49 in the experiment one was dead) qubits connected together.  

##### Pros 

These qubits are controllable using external drives meaning we can perform many types of gates on them and the parameters of the systems mean that these gates are very quick (nano seconds in length). They have the advantage that they can be fabricated using techniques already available since they are made on silicon chips. 

##### Cons 

Unfortunately the coherence time of these qubits isn't as long as we would like, it is in the range of 10's of micro seconds now but this is far behind the coherence times of some other architectures . Also they are currently limited to 2d configurations with limited connectivity (e.g. hexagons connections pic!) although advances are being made towards 3d architectures which would increase the qubit density significantly. 
### Ion Traps  
<figure>
	<img src="/assets/img/QC1/Trapped_Ion_QC.jpg" alt="TrappedIon" style="height:100%">
	<figcaption>A Trapped Ion Quantum Computer</figcaption>
</figure>
Ion Traps quantum computers are composed of physical ions trapped in electromagnetic fields ( as the name suggests ) these ions are manipulated by lasers which cool the ions to a temperature where they can act as Qubits and be manipulated to perform quantum gates. These ions are held in place by oscillating 3d electromagnetic fields, really this is the equivalent of a harmonic oscillator but in 3D these traps are called a Paul ion traps. Charged particles cannot be held in a stationary position by a constant electromagnetic field by Earnshaw's theorem ( which is a neat consequence of gauss law) so the trap is an oscillating saddle which constantly pushes the ion back into the middle of the trap. 

Ion trap QC have the longest coherence times and largest coherence time to gate time ratio of the advanced quantum architecture (1000 for ion traps and 200 for SCC). This makes them a very strong candidate for QC. They can also perform quantum gates to a very high fidelity having a single gate fidelity of 99.99 % and a two Qubits gate fidelity of 99.97%. Whilst these are very impressive ion traps suffer from a serious downside which is one of speed. Whilst modern computers operate at speeds in the range of ~5 GHz ion trap quantum computer operators in the MHz range. This means any speed up they may obtain from a quantum algorithm will be marred by this lack of speed. Also if an algorithm is very complicated it may take a very long time to execute. Quicker quantum gates. Can be executed on an ion trap computer fidelity of the gates decreases as the gate time decreases.

## Other types of Qubits   
### Topological Qubits / quantum computation 

<figure>
	<img src="/assets/img/QC1/TQC.png" alt="TopologicalCompWorks" style="height:100%">
	<figcaption>How a Topological Quantum Computers Works</figcaption>
</figure>
Topological quantum computing involves the manipulation of anyons, particles which are not quite bosons and not quite fermions, they are somewhere in between. This 
difference is quantified by the phase which the particles pick up when they are exchanged with each other ( or alternatively moved around a flux), bosons and fermions will pick up a phase of either 1 or –1 respectively when an anyon performs this same action they will pick up a phase which is somewhere in between these two values.  The idea of Topological Quantum Computing (TQC) is that we can use this property in the creation of qubits and logical gates.  
The Qubits themselves are the anyons described above, the gates in TQC are the results of moving these qubits around. This works since an exchange of anyons will result in a phase being picked up. This crossing of anyons is called braiding, after several braids which make up the quantum gate the anyons are paired up with other anyong (check this) to see if they annihilate each other or not. Whether or not the particles annihilate each other determines if the qubit is in the 0 or 1 state. The advantage of this type of QC is that it is much  less prone to local errors than the previously described qubits; this is because the information in the quantum computer is stored in the paths of the anyons and not the local qubits as in the other computers. 
The main issue with this type of quantum computer is that it is very hard to produce the anyons needed for these computations. Some experimental physicists think that they have produced these particles whilst others are a little more sceptical. Nevertheless Microsoft is working on creating this type of quantum computer since once the production of anyons is cracked there is no need for error correction so scaling such a quantum computer would not be as hard as with other architecture. 

### Quantum annealing  
<figure>
	<img src="/assets/img/QC1/DWave.jpeg" alt="Dwave" style="height:100%">
	<figcaption>DWaves Quantum Annealing Quantum Computer</figcaption>
</figure>
The final type of quantum computing we shall talk about here is  Quantum annealing. This is a much different type of Quantum Computer than the others discussed above since it does not rely on gate based operations to achieve its desired outcome. It also has a different speciality to the others, this type of QC is geared towards finding the minimum of a problem or performs ground state searches. This is of particular interest to chemists and biologists who would like to know the ground state of complex molecules which cannot be found on conventional computers in any reasonable time.  
The method behind this is the adiabatic theorem, the Quantum computer is prepared in a specific state and is then slowly evolved into another Hamiltonian. The idea is that due to the adiabatic theorem the system will stay in the ground state of the entire system and so when the evolution has finished the system should be in the ground state of the final Hamiltonian and so we will then have found the Ground state of the system we are searching for.  

<a href="https://www.mathjax.org">
    <img title="Powered by MathJax"
    src="https://www.mathjax.org/badge/badge.gif"
    border="0" alt="Powered by MathJax" />
</a>
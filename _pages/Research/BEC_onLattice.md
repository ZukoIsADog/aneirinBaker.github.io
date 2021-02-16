---
title: Research - BEC on a Lattice
permalink: /BECLattice/
author_profile: true
---

# Implementing a Binary Bose Einstein Condensate in Superconducting Circuits

Bose Einstein condensates are notoriously hard to create and control in experiments, controlling two BEC's in the same experiment is extremely hard. A paper from the early 2000's [1] described how it may be possible to implement a binary BEC by utilizing two hyperfine energy levels of the same atomic species. Within this theory it was theorised that topological features may be found, these were features such as Domain walls and vortices. As far as i am aware there has been no experimental implementation of this theory since it is so complicated to implement. 
In light of this we are attempting to create a Quantum Simulator of a Binary BEC using Superconducting circuits. Using superconducting circuits has the advantage that they are easily controlled and benefit from solid fabrication techniques. They are also modular and have a wide array of elements that can produce the non linear effects that we need. These non linearities help us to produce the interaction we require. As there are two species we require 4 body self interactions within the species and four body interactions between the species. Four body interactions have been proven theoretically [2] to occur in SCC's and four body interaction between two species have been shown to exist as well [3].


## Outcomes

We aim to show that it may be possible to detect topological features within superconducting circuits and prove the theoretical basis that was laid down. We also aim to extend the parameter range that Trapped Ion physicists are able to probe with their experiments. This could lead to new and interesting phases of matter and deepen our understanding of both BEC's and Quantum Simulators. This would also be a great experimental challenge since controlling many qubits on a single chip is vary hard and the number of qubits is currently one of the limiting factors facing the development of Quantum COmputers today. 

<hr>

### References

[1] - Son, D. T., & Stephanov, M. A. (2002). Domain walls of relative phase in two-component Bose-Einstein condensates. Physical Review A - Atomic, Molecular, and Optical Physics, 65(6), 636211–63621110. https://doi.org/10.1103/PhysRevA.65.063621

[2] - Sameti, M., Potočnik, A., Browne, D. E., Wallraff, A., & Hartmann, M. J. (2017). Superconducting quantum simulator for topological order and the toric code. Physical Review A, 95(4), 1–20. https://doi.org/10.1103/PhysRevA.95.042330

[3] - Collodo, M. C., Potočnik, A., Gasparinetti, S., Besse, J. C., Pechal, M., Sameti, M., … Eichler, C. (2019). Observation of the Crossover from Photon Ordering to Delocalization in Tunably Coupled Resonators. Physical Review Letters, 122(18), 1–6. https://doi.org/10.1103/PhysRevLett.122.183601


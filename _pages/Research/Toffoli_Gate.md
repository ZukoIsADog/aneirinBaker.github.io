---
title: Research - Toffoli Gate
permalink: /Toffoli/
author_profile: true
---

## Many Body Operations within Superconducting Circuits 

Quantum Superconducting circuits are a possibility for the basic archecture of Quantum Computers [1] . Currently they exhibit 1 and 2 body interactions (4 is a possibility but not implemented [2]). These types of Quantum Computers operator on a Gate based system where gates (operations) are applied to groups of Qubits to execute Qunatum algorithms.

Gates which apply to more than 2 Qubits are decomposed inot 1 & 2 gates to be executed. This effects the gate time and gate fidelity we aim to combat this by producing a circuit which can perform 1,2 and 3 body interactions. This would make Multi Body gates mich quicker and produce a higher Fidelity.

<table cellspacing="0" cellpadding="0" border="0">
        <td style="text-align: center;">
            <img src="../../assets/img/Research/Toffoli_Comparison.png" alt="" />
            <br />
            <a >Toffoli gate executed on a SCC and an Ion Trap Quantum Computer [3]</a>
        </td>
</table>

As it can be seen above the Toffoli gate performed on the IBM Quantum Computer [3] has a fidelity much lower than the Ion Trap QC which is to be expected. We aim to imporve on this by using a flux-qubit type element along with theoritical procedures developed in my PhD to perform this gate opertaion much quiker and with a higher fidelity. 
<table cellspacing="0" cellpadding="0" border="0">
	<td style="text-align: center;">
        <img src="../../assets/img/Research/Toff_Decomp.png" alt="" />
        <br />
        <a>Toffoli decomposition into 1 and 2 body gates.</a>
    </td>
</table>

To do this we attempt to perform the gate in a single shot using the circuit we designed that can perform all interactions up to third order. This is exactly what you need for the decomposition of the Three qubit Toffoli gate however these interaction are very small as the interaction strength scales inversely to the number of qubits in the interaction. This here is where our challenge lies, we need to design a procedure where in we can make use of the small three body interaction without other interaction over powering them. 

## Update Feb 2022
This research has now been publised. You can find the article <a href="https://doi.org/10.1063/5.0077443">here</a> 

### References

[1] - Arute, F., Arya, K., Babbush, R., Bacon, D., Bardin, J. C., Barends, R., … Martinis, J. M. (2019). Quantum supremacy using a programmable superconducting processor. Nature, 574(7779), 505–510. https://doi.org/10.1038/s41586-019-1666-5

[2] - Sameti, M., Potočnik, A., Browne, D. E., Wallraff, A., & Hartmann, M. J. (2017). Superconducting quantum simulator for topological order and the toric code. Physical Review A, 95(4), 1–20. https://doi.org/10.1103/PhysRevA.95.042330

[3] - Linke, Norbert Matthias et al. “Experimental comparison of two quantum computing architectures.” Proceedings of the National Academy of Sciences 114 (2017): 3305 - 3310.

[4] - IBM Q - Quantum Computing. (n.d.). Retrieved May 13, 2019, from https://www.research.ibm.com/ibm-q/


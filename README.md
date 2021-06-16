#  IBM-QUANTUM-CHALLANGE--2021SOLUTION
I completed all 5 exercises in the IBM Quantum Challenge 2021 - and this is the solution
The IBM Quantum Challenge 2021 took place from 05/20 to 05/26/2021, and its theme was the celebration of 40 years of the 1981 Computer Physics Conference and the 5 years of quantum computing in the IBM cloud.
 There were 5 exercises, with themes that marked these 40 years of quantum computing.
## Exercise 1 - Toffoli gate
we want to build a Toffoli gate as well. Why the Toffoli gate? As mentioned above, the Toffoli gate is also a universal gate for classical computation the same way the NAND gate is, but it is reversible. Further it builds a simple universal gate set for quantum computation if combined with the Hadamard gate.

## Exercise 2 - Shor's algorithm
###The problem
In this exercise, we will factor 35 by doing phase estimation on a circuit that implements 13𝑦mod35. The exercise is to create a circuit that does this, and is also small enough to run on ibmq_santiago! This is not an easy task
## Exercise 3 - Quantum error correction
### The problem of errors
Errors occur when some spurious operation acts on our qubits. Their effects cause things to go wrong in our circuits. The strange results you may have seen when running on real devices is all due to these errors.

There are many spurious operations that can occur, but it turns out that we can pretend that there are only two types of error: bit flips and phase flips.

Bit flips have the same effect as the x gate. They flip the |0⟩ state of a single qubit to |1⟩ and vice-versa. Phase flips have the same effect as the z gate, introducing a phase of −1 into superpositions. Put simply, they flip the |+⟩ state of a single qubit to |−⟩ and vice-versa.

The reason we can think of any error in terms of just these two is because any error can be represented by some matrix, and any matrix can be written in terms of the matrices 𝑋 and 𝑍. Specifically, for any single qubit matrix 𝑀,

𝑀=𝛼𝐼+𝛽𝑋+𝛾𝑋𝑍+𝛿𝑍,
for some suitably chosen values 𝛼, 𝛽, 𝛾 and 𝛿.

So whenever we apply this matrix to some single qubit state |𝜓⟩ we get

𝑀|𝜓⟩=𝛼|𝜓⟩+𝛽𝑋|𝜓⟩+𝛾𝑋𝑍|𝜓⟩+𝛿𝑍|𝜓⟩.
The resulting superposition is composed of the original state, the state we'd have if the error was just a bit flip, the state for just a phase flip and the state for both. If we had some way to measure whether a bit or phase flip happened, the state would then collapse to just one possibility. And our complex error would become just a simple bit or phase flip.

So how do we detect whether we have a bit flip or a phase flip (or both). And what do we do about it once we know? Answering these questions is what quantum error correction is all about.
####GOAL
Create circuits which can detect x and z errors on two qubits. You can come up with a solution of your own. Or just tweak the almost valid solution given below.
## Exercise 4 - Transmon qubit
####GOAL

Find |1⟩→|2⟩ transition frequency 𝑓12.

Plan

1-(Tutorial) Find |0⟩→|1⟩ transition frequency 𝑓01 using spectroscopy (sweeping frequency).
2-(Tutorial) Calibrate X-180 pulse amplitude using Rabi oscillation (sweeping amplitude).
3-(Problem) Find |1⟩→|2⟩ transition frequency 𝑓12 using the calibrated X-180 pulse and spectroscopy (sweeping frequency).
## Exercise 5 - Variational quantum eigensolver
####GOAL

Find the shortest ansatz circuits for representing accurately the ground state of given problems. Be creative!

Plan

First you will learn how to compose a VQE simulation for the smallest molecule and then apply what you have learned to a case of a larger one.

1. Tutorial - VQE for H2: familiarize yourself with VQE and select the best combination of ansatz/classical optimizer by running statevector simulations.

2. Final Challenge - VQE for LiH: perform similar investigation as in the first part but restricting to statevector simulator only. Use the qubit number reduction schemes available in Qiskit and find the optimal circuit for this larger system. Optimize the circuit and use your imagination to find ways to select the best building blocks of parameterized circuits and compose them to construct the most compact ansatz circuit for the ground state, better than the ones already available in Qiskit.

g blocks of parameterized circuits and compose them to construct the most compact ansatz circuit for the ground state, better than the ones already available in Qiskit.

## Thank you very much for following me on my IBM Quantum Challenge 2021 journey, I hope some of what I said was helpful for as many people as possible. This year’s challenge was a great opportunity to learn and further our Qiskit skills together as a community. Over 1400 participants submitted at least one answer which is a great testament to the challenge as a whole.
One big final thanks to the organisers of the challenge!!!



# Quantum Coalition Hack IBM Quantum Technical Callenge
##  Problem statement:

Qiskit Pulse allows you to program real quantum computers at the pulse level. Namely, it provides a language for specifying the microwave control tones (i.e. control of the continuous time dynamics of input signals) that program the quantum state.

In most quantum algorithms/applications, computations are carried out over a 2^n-dimensional Hilbert space spanned by {|0>,|1⟩}^n, where n is the number of qubits. In IBM's quantum hardware, however, there also exists higher energy states which are typically avoided. (e.g. the single qubit "DRAG" pulse helps reduce unintentionally occupation in the |2> state).

In this challenge we want you to use Qiskit Pulse to explore the higher energy states, and put together a unique project which shows how that higher energy state directly benefits or makes your idea possible.

The best application of this idea will be the winner. Preference will be given to projects that - use Qiskit and/or IBM Quantum's devices - explain issues faced, problem your team overcame, and future implications of your project - show how your project could benefit the quantum computing community - delve into why this is important for future research or applications

IBM Quantum will award custom swag prizes to the winning teams. Total number of teams receiving a prize will be determined by how many total projects are submitted. Note - All projects submitted must be using Qiskit version 0.25. Anyone can submit a project, however someone working for a GOE, i.e. Government Owned Entity, will not be eligible for prizes or awards. Full eligibility rules here.

## Project overview:

With this project I intend to use a higher energy state (the 2 state) to perform random number generation and afterwards a quantum random optimization of an objective function to find a maximum value. The main difference between this implementation and an implementation using only the $ |0&gt; $ and $ |1&gt; $ states is the potential increase of available random numbers for the same amount of qubits. The random number generator implemented in this notebook already works on circuits to create any of $ 2^n $ different random numbers, where n is the amount of qubits. With the inclusion of the $ |2&gt; $ state, the same algorithm may create any of $ 3^n $ different random numbers, an important increase that can be useful for creating more quality random numbers on NISQ computers with a small amount of qubits, like on the ibmq_bogota device that has 5 qubits. The amount of unique random numbers obtainable using the ibmq_bogota device went from $ 2^5 = 32 $ to $ 3^5 = 243 $.
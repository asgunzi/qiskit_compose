# qiskit_compose
Example of compose function in Qiskit

The “compose” function is used to join two circuits q_1 and q_2.
Let qc_1:

![](https://informacaoquantica.files.wordpress.com/2021/06/qc_1.png)

And qc_2:
![](https://informacaoquantica.files.wordpress.com/2021/06/qc_2.png)
To join 1 and 2, just use the following code:

qc = qc_1.compose(qc_2)
![](https://informacaoquantica.files.wordpress.com/2021/06/qc_composed.png)

An alternative method, already deprecated, is to use the summation:
qc = qc_1 + qc_2
Compose has the advantage of being more general. It is possible to change the “wiring” of the circuit:
qc = qc_1.compose(qc_2, qubits =[0,2,1,3])
![](https://informacaoquantica.files.wordpress.com/2021/06/Compose_Rewiring.png)

It is also possible to join a circuit with fewer qubits to a circuit with more qubits, indicating how they are wired together. If it is the opposite, joining a circuit with more qubits to another one with less, will give an error — the trick is to invert the composition of the circuit and use the option Front = True.
Qiskit Documentation:
https://qiskit.org/documentation/stubs/qiskit.circuit.QuantumCircuit.html#qiskit.circuit.QuantumCircuit.compose
Example code:
https://github.com/asgunzi/qiskit_compose

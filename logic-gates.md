# Logic Gates

## Introduction

A logic gate is an elementary building block of a digital circuit. Most logic gates have two inputs and one output. At any given moment, every terminal is in one of the two binary conditions low (0) or high (1), represented by different voltage levels. The logic state of a terminal can, and generally does, change often, as the circuit processes data. In most logic gates, the low state is approximately zero volts (0 V), while the high state is approximately five volts positive (+5 V). There are seven basic logic gates: AND, OR, NOT, NAND, NOR, XOR, and XNOR. The AND, OR, and NOT gates are the basic logic gates. The NAND, NOR are the universal gates. The XOR and XNOR gates are the special gates.

## AND Gate

The output is high only when all inputs are high.

$$
Y = A \cdot B
$$

Truth Table:

$$
\begin{array}{|cc|c|}
\hline
\text{A} & \text{B} & \text{AB} \\
\hline
0 & 0 & 0 \\
0 & 1 & 0 \\
1 & 0 & 0 \\
1 & 1 & 1 \\
\hline
\end{array}
$$

## OR Gate

The output is high when any of the inputs are high.

$$
Y = A + B
$$

Truth Table:

$$
\begin{array}{|cc|c|}
\hline
\text{A} & \text{B} & \text{A+B} \\
\hline
0 & 0 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
1 & 1 & 1 \\
\hline
\end{array}
$$

## NOT Gate

It is also called an inverter. The output is the inverse of the input.

$$
Y = A'
$$

Truth Table:

$$
\begin{array}{|c|c|}
\hline
\text{A} & \text{A'} \\
\hline
0 & 1 \\
1 & 0 \\
\hline
\end{array}
$$

## NAND Gate

It is the combination of AND and NOT gates. The output is high when any of the inputs are low.

$$
Y = (A \cdot B)'
$$

Truth Table:

$$
\begin{array}{|cc|c|c|}
\hline
\text{A} & \text{B} & \text{AB} & \text{(AB)'} \\
\hline
0 & 0 & 0 & 1 \\
0 & 1 & 0 & 1 \\
1 & 0 & 0 & 1 \\
1 & 1 & 1 & 0 \\
\hline
\end{array}
$$

## NOR Gate

It is the combination of OR and NOT gates. The output is high only when all inputs are low.

$$
Y = (A + B)'
$$

Truth Table:

$$
\begin{array}{|cc|c|c|}
\hline
\text{A} & \text{B} & \text{A+B} & \text{(A+B)'} \\
\hline
0 & 0 & 0 & 1 \\
0 & 1 & 1 & 0 \\
1 & 0 & 1 & 0 \\
1 & 1 & 1 & 0 \\
\hline
\end{array}
$$

## XOR Gate

This is also known as the exclusive OR gate.
For two inputs, the output is high when the inputs are different and the output is low when the inputs are the same. It is used as an inequality detector.

$$
Y = A \oplus B = A'B + AB'
$$

Truth Table:

$$
\begin{array}{|cc|c|}
\hline
\text{A} & \text{B} & \text{A⊕B} \\
\hline
0 & 0 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
1 & 1 & 0 \\
\hline
\end{array}
$$

For more than two inputs, the output is high when the number of high inputs is odd. And the output is low when the number of high inputs is even.

$$
Y = A \oplus B \oplus C = A'B'C + A'BC' + AB'C' + ABC
$$

Truth Table:

$$
\begin{array}{|ccc|c|}
\hline
\text{A} & \text{B} & \text{C} & \text{A⊕B⊕C} \\
\hline
0 & 0 & 0 & 0 \\
0 & 0 & 1 & 1 \\
0 & 1 & 0 & 1 \\
0 & 1 & 1 & 0 \\
1 & 0 & 0 & 1 \\
1 & 0 & 1 & 0 \\
1 & 1 & 0 & 0 \\
1 & 1 & 1 & 1 \\
\hline
\end{array}
$$

TODO: XOR gate using basic gates.

We can use a XOR gate to implement an inverter. If we connect one input of the XOR gate to a constant high value, we get an inverter. The output is the inverse of the input.

$$
Y = A \oplus 1 = A'
$$

## XNOR Gate

This is also known as the exclusive NOR gate.
For two inputs, the output is high when the inputs are the same and the output is low when the inputs are different. It is also used as an equality detector.

$$
Y = A \odot B = AB + A'B' = (A \oplus B)'
$$

Truth Table:

$$
\begin{array}{|cc|c|}
\hline
\text{A} & \text{B} & \text{A⊙B} \\
\hline
0 & 0 & 1 \\
0 & 1 & 0 \\
1 & 0 & 0 \\
1 & 1 & 1 \\
\hline
\end{array}
$$

For more than two inputs, the output is high when the number of high inputs is even. And the output is low when the number of high inputs is odd.

$$
Y = A \odot B \odot C = A'B'C' + A'BC + AB'C + ABC'
$$

Truth Table:

$$
\begin{array}{|ccc|c|}
\hline
\text{A} & \text{B} & \text{C} & \text{A⊙B⊙C} \\
\hline
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0 \\
0 & 1 & 0 & 0 \\
0 & 1 & 1 & 1 \\
1 & 0 & 0 & 0 \\
1 & 0 & 1 & 1 \\
1 & 1 & 0 & 1 \\
1 & 1 & 1 & 0 \\
\hline
\end{array}
$$

TODO: XNOR gate using basic gates.

We can use a XNOR gate to implement an inverter. If we connect both inputs of the XNOR gate, we get an inverter. The output is the inverse of the input.

$$
Y = A \odot A = A'
$$

## NAND Gate as Universal Gate

### Inverter using NAND

We can use a NAND gate to implement an inverter. If we connect both inputs of the NAND gate, we get an inverter. The output is the inverse of the input.

$$
Y = A \cdot A = A'
$$

### AND Gate using NAND

We can use two NAND gates to implement an AND gate. If we connect the output of the first NAND gate to the input of the second NAND gate, we get an AND gate.

$$
Y_1 = (A \cdot B)'
Y_2 = Y_1 \cdot Y_1 = A \cdot B
$$

### OR Gate using NAND

We can use three NAND gates to implement an OR gate. If we connect A to the first NAND gate, B to the second NAND gate, we will get $A'$ and $B'$ as outputs. If we connect the outputs of the first and second NAND gates to the third NAND gate, we get an OR gate.

$$
Y_1 = A \cdot A = A'
Y_2 = B \cdot B = B'
Y_3 = Y_1 \cdot Y_2 = A' \cdot B' = \overline{A' \cdot B'} = A + B
$$

### NOR Gate using NAND

TODO

### XOR Gate using NAND

TODO: Important

### XNOR Gate using NAND

TODO

## NOR Gate as Universal Gate

TODO


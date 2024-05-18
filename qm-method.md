# QM Method

## Quine-McCluskey Algorithm

Quine McCluskey minimization method, is a technique for reducing for minimizing the expression in their SOP (sum of product) or POS (product of sum) form. Also called a tabular method, this method has advantages over the K-Map method, in case the number of input variables is large. For an input variable greater than six, the K Map method becomes more complex. For such problems, McCluskey or Tabular method has a simplified approach. The McCluskey method can be used to design complex circuits in digital systems.

* It is a tabular method
* No visualization of prime implicants
* Can be programmed and implemented in a computer

### Example 01

$$
Y(A,B,C,D) = \sum m(0, 1, 3, 7, 8, 9, 11, 15)
$$

Step 1: Write the minterms in binary form.

Step 2: Group the minterms(and don't cares) according to the number of 1s in their binary form.

Step 3: Compare the minterms in adjacent groups. If two minterms differ in only one bit, then they are combined to form a new group. The new group is formed by replacing the differing bit with a dash or d.

Step 4: Repeat step 3 until no more groups can be formed.

Step 5: The minterms in each group are combined to form a prime implicant. The prime implicants are then combined to form the essential prime implicants and the non-essential prime implicants (don't cares excluded).

Step 6: The essential prime implicants are combined to form the minimum sum of products expression.

Step 1 & 2:

$$
\begin{array}{|c|c|c|c|}
\hline
Group & Minterm & A B C D & Matched \\
\hline
0 & m_0 & 0 0 0 0 & ✅ \\
\hline
1 & m_1 & 0 0 0 1  & ✅ \\
& m_8 & 1 0 0 0 & ✅ \\
\hline
2 & m_3 & 0 0 1 1 & ✅ \\
& m_9 & 1 0 0 1 & ✅ \\
\hline
3 & m_7 & 0 1 1 1 & ✅ \\
& m_{11} & 1 0 1 1 & ✅ \\
\hline
4 & m_{15} & 1 1 1 1 & ✅ \\
\hline
\end{array}
$$


Step 3 & 4:

{% tabs %}
{% tab title="Table 1" %}

$$
\begin{array}{|c|c|cccc|c|}
\hline
Group & Matched\, Pair & A&B&C&D & Matched \\
\hline
0 & m_0,m_1 & 0&0&0&d & ✅ \\
& m_0,m_8 & d&0&0&0 & ✅ \\
\hline
1 & m_1,m_3 & 0&0&d&1 & ✅ \\
& m_1,m_9 & d&0&0&1 & ✅ \\
& m_8,m_9 & 1&0&0&d & ✅ \\
\hline
2 & m_3,m_7 & 0&d&1&1 & ✅ \\
& m_3,m_{11} & d&0&1&1 & ✅ \\
& m_9,m_{11} & 1&0&d&1 & ✅ \\
\hline
3 & m_7,m_{15} & d&1&1&1 & ✅ \\
& m_{11},m_{15} & 1&d&1&1 & ✅ \\
\hline
\end{array}
$$
{% endtab %}

{% tab title="Table 2" %}

$$
\begin{array}{|c|c|cccc|c|}
\hline
Group & Matched\, Pair & A&B&C&D & Prime\, Imp \\
\hline
0 & m_0,m_1, m_8,m_9 & d&0&0&d & B'C' \\
& m_0,m_8, m_1,m_9 & d&0&0&d & \\
\hline
1 & m_1,m_3, m_9,m_{11} & d&0&d&1 & B'C \\
& m_1,m_9, m_3,m_{11} & d&0&d&1 & \\
\hline
3 & m_3,m_7, m_{11},m_{15} & d&d&1&1 & CD \\
& m_3,m_{11}, m_7,m_{15} & d&d&1&1 & \\
\hline
\end{array}
$$
{% endtab %}
{% endtabs %}

Step 5:

We will find the single cross mark in each column and mark them. These rows are the essential prime implicants.

$$
\begin{array}{|c|c|cccccccc|}
\hline
Prime\,Imp & Minterms & 0 & 1 & 3 & 7 & 8 & 9 & 11 & 15 \\
\hline
B'C' & 0, 1, 8, 9 & [x] & x & 3 & 7 & [x] & x & 11 & 15 \\
\hline
B'D & 1, 3, 9, 11 & 0 & x & x & 7 & 8 & x & x & 15 \\
\hline
CD & 3, 7, 11, 15 & 0 & 1 & x & [x] & 8 & 9 & x & [x] \\
\hline
\end{array}
$$

The boolean expression is,

$$
Y = B'C' + CD
$$

### Example 02

$$
F(W,X,Y,Z) = \sum m(0, 3, 5, 6, 7, 10, 12, 13) + \sum d(2, 9, 15)
$$

Step 1 & 2:

$$
\begin{array}{|c|c|cccc|c|}
\hline
Group & Minterm & W&X&Y&Z & Matched \\
\hline
G_0 & m_0 & 0&0&0&0 & ✅ \\
\hline
G_1 & m_2 & 0&0&1&0 & ✅ \\
\hline
G_2 & m_3 & 0&0&1&1 & ✅ \\
& m_5 & 0&1&0&1 & ✅ \\
& m_6 & 0&1&1&0 & ✅ \\
& m_9 & 1&0&0&1 & ✅ \\
& m_{10} & 1&0&1&0 & ✅ \\
& m_{12} & 1&1&0&0 & ✅ \\
\hline
G_3 & m_7 & 0&1&1&1 & ✅ \\
& m_{13} & 1&1&0&1 & ✅ \\
\hline
G_4 & m_{15} & 1&1&1&1 & ✅ \\
\hline
\end{array}
$$

Step 3 & 4:

$$
\begin{array}{|c|c|cccc|c|}
\hline
Group & Matched\, Pair & W&X&Y&Z & Matched \\
\hline
G_0' & m_0,m_2 & 0&0&d&0 & ✅ \\
\hline
G_1' & m_2,m_3 & 0&0&d&d & ✅ \\
& m_2,m_6 & 0&0&d&d & ✅ \\
& m_2,m_{10} & 0&0&d&d & ✅ \\
\hline
G_2' & m_3,m_7 & 0&d&1&1 & ✅ \\
& m_5,m_7 & 0&d&0&1 & ✅ \\
& m_5,m_{13} & 0&d&0&1 & ✅ \\
& m_6,m_7 & 0&d&1&0 & ✅ \\
& m_9,m_{13} & 1&d&0&1 & ✅ \\
& m_{12},m_{13} & 1&d&0&1 & ✅ \\
\hline
G_3' & m_7,m_{15} & d&d&1&1 & ✅ \\
& m_{13},m_{15} & 1&d&0&d & ✅ \\
\hline
\end{array}
$$

$$
\begin{array}{|c|c|cccc|c|}
\hline
Group & Matched\, Pair & W&X&Y&Z & Matched \\
\hline
G_1'' & m_2,m_3,m_6,m_7 & 0&0&d&d & ✅ \\
& m_2,m_6,m_3,m_7 & 0&0&d&d & \\
\hline
G_2'' & m_5,m_7,m_{13},m_{15} & 0&d&0&1 & ✅ \\
& m_5,m_{13},m_7,m_{15} & 0&d&0&1 & \\
\hline
\end{array}
$$

$$
\begin{array}{|c|c|cccc|c|}
\hline
Group & Matched\, Pair & W&X&Y&Z & Prime\, Imp \\
\hline
G_0''' & m_0,m_2 & 0&0&d&0 & W'X'Z \\
\hline
G_1'' & m_2,m_3,m_6,m_7 & 0&0&d&d & W'X' \\
& m_2,m_{10},m_3,m_7 & 0&0&d&d & \\
\hline
G_2'' & m_5,m_7,m_{13},m_{15} & 0&d&0&1 & WX'Z \\
& m_9,m_{13} & 1&d&0&1 & \\
& m_{12},m_{13} & 1&d&0&1 & \\
\hline
\end{array}
$$

Step 5:

$$
\begin{array}{|c|c|cccccccc|}
\hline
Prime\,Imp & Minterms & 0 & 2 & 3 & 5 & 6 & 7 & 9 & 10 & 12 & 13 & 15 \\
\hline
W'X'Z & 0, 2 & [x] & x & x & x & x & x & x & x & x & x & x \\
\hline
W'X' & 2, 3, 6, 7 & 0 & [x] & x & x & x & x & x & x & x & x & x \\
\hline
WX'Z & 5, 7, 13, 15 & 0 & x & x & [x] & x & [x] & x & x & x & x & [x] \\
\hline
\end{array}
$$

The boolean expression is,

$$
F = W'X'Z + WX'Z
$$


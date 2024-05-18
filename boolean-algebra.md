# Boolean Algebra

## Introduction

It is the set of rules used to simplify the given logic expression without changing its functionality. It is used when number of variables are less. A variable whose value can be either 1 or 0 is called a `Boolean variable`.

AND, OR , NOT are the basic Boolean operations. We can express Boolean functions with either an expression or a truth table. Every Boolean expression can be converted to a circuit.

* AND is denoted by a dot ( . ).
* OR is denoted by a plus ( + ).
* NOT is denoted by an over bar ( $$\overline A$$ ) , a single quote mark ( ' ), or tilde sign ( \~ ) before the variable.

Truth table for basic logic operation:

{% tabs %}
{% tab title="AND" %}
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

{% endtab %}

{% tab title="OR" %}
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
{% endtab %}

{% tab title="NOT" %}
$$
\begin{array}{|c|c|}
\hline
\text{A} & \sim \text{A} \\
\hline
0 & 1 \\
1 & 0 \\
\hline
\end{array}
$$
{% endtab %}
{% endtabs %}



The order of evaluation is:

1. Parentheses
2. NOT
3. AND
4. OR

Consequence: Parentheses appear around OR expressions. Example,

```
F = A(B+C)(C+D)
```

### Boolean Algebra Postulates

* Identity Law -> $$A+0=A \quad and \quad A.1=A$$
* Domination Law -> $$A+1=1 \quad and \quad A.0=0$$
* Idempotent Law -> $$A+A=A \quad and \quad A.A=A$$
* Complement Law -> $$A+\overline A=1 \quad and \quad A.\overline A=0$$
* Commutative Law -> $$A+B=B+A \quad and \quad A.B=B.A$$
* Associative Law -> $$A+(B+C)=(A+B)+C \quad and \quad A.(B.C)=(A.B).C$$
* Distributive Law -> $$A.(B+C) = A.B+A.C \quad and \quad A+B.C=(A+B).(A+C)$$
* Absorption Theorem
* De Morgan's Theorem
* Redundancy Theorem

### De Morgan's Theorem

$$
( A . B)' = A' + B' \quad and \quad ( A + B)' = A'.B'
$$

#### Example 1

$$
\begin{align*}
    F   &= \overline{A+\overline{B}C} \\
        &= \overline{A}\,(\overline{\overline{B}C}) \\
        &= \overline{A}\,(\overline{\overline{B}}+\overline{C}) \\
        &= \overline{A}\,(B+\overline{C})
\end{align*}
$$

#### Example 2

$$
\begin{align*}
    F   &= \overline{(A+C)(A+\overline{B})(\overline{A}+B+\overline{C})} \\
        &= \text{TODO}
\end{align*}
$$

### Absorption Theorem

$$
A(A+B)=A \quad and \quad A+A.B=A
$$

### Redundancy Theorem

It is also called the Consensus Theorem. It states that a term can be added or subtracted from a Boolean expression without changing the expression.

$$
Y = AB + A'C + BC = AB + A'C
$$

### Duality Principle

If an algebraic expression is true for all possible values of the variables, then the dual of the expression is also true for all possible values of the variables. The dual of an expression is obtained by interchanging the AND and OR operators and replacing the variables by their complements.

```text
OR <=> AND
0 <=> 1
```

Example:

$$
\begin{align*}
    F   &= A+B \\
    F'  &= A'.B'
\end{align*}
$$


## Logic Gate

In the earliest computers, switches were opened and closed by magnetic fields produced by energizing coils in relays. The switches in turn opened and closed the current paths. Later, vacuum tubes were used to open and close current paths electronically to replace relays. Today, transistors are used as electronic switches that open and close current paths.

### Symbols

<div align="center">

<figure><img src=".gitbook/assets/boolean-algebra/AND.jpg" alt="AND Gate" width="188"><figcaption><p>AND Gate</p></figcaption></figure>

 

<figure><img src=".gitbook/assets/boolean-algebra/OR.jpg" alt="" width="188"><figcaption><p>OR Gate</p></figcaption></figure>

 

<figure><img src=".gitbook/assets/boolean-algebra/NOT.jpg" alt="" width="188"><figcaption><p>NOT Gate</p></figcaption></figure>

</div>

## Boolean Functions

A Boolean function is a function whose arguments, as well as the function itself, assume values from a two-element set {0, 1}. Example:

```text
F(X, Y) = X'Y' + XY + X'Y
```

### Some examples

Example 1:

$$
\begin{align*} F &= A.B + A.B' \\ &= A(B+B') \\ &= A.1 \\ &= A \end{align*}
$$

$$
\begin{array}{|cc|c|}
\hline
\text{A} & \text{B} & F=A.B + A.\overline{B} \\
\hline
0 & 0 & 0 \\
0 & 1 & 0 \\
1 & 0 & 1 \\
1 & 1 & 1 \\
\hline
\end{array}
$$

Example 2:

$$
\begin{align*} F &= A.B + A.B'C + AB'C' \\ &= A(B+B'C+B'C') \\ &= A(B+C+B'C') \quad \text{Distributive law} \\ 
&= A(B+C+C') \quad \text{Distributive law} \\ 
&= A(B+1) \\ &= A.1 \\ &= A \end{align*}
$$

Example 3:

$$
\begin{align*}
    F   &= (A+B+C)(A+B'+C)(A+B+C') \\
        &= (A+B+C)(A+B+C')(A+B'+C) \quad \text{Commulative law} \\
        &= (X+C.C')(A+B'+C) \quad let, \quad X=A+B \quad \text{Distributive law} \\
        &= (X+0)(A+B'+C) \\
        &= X(A+B'+C) \\
        &= (A+B)(A+B'+C) \\
        &= A+B(B'+C) \\
        &= A + B.B' + BC \\
        &= A + 0 + C \\
        &= A+C
\end{align*}
$$

Example 4:

$$
\begin{align*}
    F   &= (A+B)(A+B')(A'+B)(A'B') \\
        &= (A + B.B')(A'+B.B') \\
        &= (A+0)(A'+b) \\
        &= A.A' \\
        &= 0
\end{align*}
$$

Example 5:

$$
\begin{align*}
    F   &= A.B + A'.C + B.C \\
        
\end{align*}
$$

## Boolean Function Representation

There are two ways to convert truth tables to Boolean functions:

* Using Sum of Products(SOP) / Minterms
* Using Product of Sums(POS) / Maxterms


## Canonical Form and Non-Canonical Form

* Canonical form: A Boolean function is in canonical form if it is expressed as a sum of minterms or product of maxterms where all the variables are present in each term.
* Non-canonical form: A Boolean function is in non-canonical form if it is expressed as a sum of maxterms or product of minterms where all the variables are not present in each term.

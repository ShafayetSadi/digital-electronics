# Boolean Algebra

## Introduction

It is the set of rules used to simplify the given logic expression without changing its functionality. It is used when number of variables are less. A variable whose value can be either 1 or 0 is called a Boolean variable.

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
        &= TODO
\end{align*}
$$

### Absorption Theorem

$$
A(A+B)=A \quad and \quad A+A.B=A
$$

### Redundancy Theorem


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

{% tabs %}
{% tab title="Example 1" %}

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

{% endtab %}

{% tab title="Example 2" %}

{% endtab %}
{% endtabs %}

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


### Canonical Form and Non-Canonical Form

* Canonical form: A Boolean function is in canonical form if it is expressed as a sum of minterms or product of maxterms where all the variables are present in each term.
* Non-canonical form: A Boolean function is in non-canonical form if it is expressed as a sum of maxterms or product of minterms where all the variables are not present in each term.


### Minterm

In canonical form of SOP, each term is called a minterm. A minterm is a product of all the variables in the function in either normal or complemented form.

* Product (AND function)
* Contains all variables
* Evaluates to '1' for a specific combination

Two variable minterms:
$$
\begin{array}{|c|c|c|c|}
\hline
A & B & minterms & Notation \\
\hline
0 & 0 & A'B' & m_0 \\
0 & 1 & A'B & m_1 \\
1 & 0 & AB' & m_2 \\
1 & 1 & AB & m_3 \\
\hline
\end{array}
$$

Three variable minterms:
$$
\begin{array}{|c|c|c|c|c|}
\hline
A & B & C & minterms & Notation \\
\hline
0 & 0 & 0 & A'B'C' & m_0 \\
0 & 0 & 1 & A'B'C & m_1 \\
0 & 1 & 0 & A'BC' & m_2 \\
0 & 1 & 1 & A'BC & m_3 \\
1 & 0 & 0 & AB'C' & m_4 \\
1 & 0 & 1 & AB'C & m_5 \\
1 & 1 & 0 & ABC' & m_6 \\
1 & 1 & 1 & ABC & m_7 \\
\hline
\end{array}
$$

#### Example of Minterm

$$
\begin{array}{|ccc|c|}
\hline
\text{A} & \text{B} & \text{C} & \text{F} \\
\hline
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0 \\
0 & 1 & 0 & 1 \\
0 & 1 & 1 & 0 \\
1 & 0 & 0 & 1 \\
1 & 0 & 1 & 0 \\
1 & 1 & 0 & 0 \\
1 & 1 & 1 & 1 \\
\hline
\end{array}
$$

From the truth table, the Boolean function is:

$$
\begin{align*}
    F   &= A'B'C' + A'BC' + AB'C' + ABC \\
        &= m_0 + m_2 + m_4 + m_7 \\
        &= \sum(0, 2, 4, 7)
\end{align*}
$$


### Maxterm

In canonical form of POS, each term is called a maxterm. A maxterm is a sum of all the variables in the function in either normal or complemented form.

* Sum (OR function)
* Contains all variables
* Evaluates to '0' for a specific combination

Two variable maxterms:
$$
\begin{array}{|c|c|c|c|}
\hline
A & B & maxterms & Notation \\
\hline
0 & 0 & A+B & M_0 \\
0 & 1 & A+B' & M_1 \\
1 & 0 & A'+B & M_2 \\
1 & 1 & A'+B' & M_3 \\
\hline
\end{array}
$$

Three variable maxterms:
$$
\begin{array}{|c|c|c|c|c|}
\hline
A & B & C & maxterms & Notation \\
\hline
0 & 0 & 0 & A+B+C & M_0 \\
0 & 0 & 1 & A+B+C' & M_1 \\
0 & 1 & 0 & A+B'+C & M_2 \\
0 & 1 & 1 & A+B'+C' & M_3 \\
1 & 0 & 0 & A'+B+C & M_4 \\
1 & 0 & 1 & A'+B+C' & M_5 \\
1 & 1 & 0 & A'+B'+C & M_6 \\
1 & 1 & 1 & A'+B'+C' & M_7 \\
\hline
\end{array}
$$

#### Example of Maxterm

$$
\begin{array}{|ccc|c|c|}
\hline
\text{A} & \text{B} & \text{C} & \text{F} & \text{F'} \\
\hline
0 & 0 & 0 & 1 & 0 \\
0 & 0 & 1 & 0 & 1 \\
0 & 1 & 0 & 1 & 0 \\
0 & 1 & 1 & 0 & 1 \\
1 & 0 & 0 & 1 & 0 \\
1 & 0 & 1 & 0 & 1 \\
1 & 1 & 0 & 0 & 1 \\
1 & 1 & 1 & 1 & 0 \\
\hline
\end{array}
$$

From the truth table, the Boolean function is:
$$
\begin{align*}
    F'              &= A'B'C + A'BC + AB'C + ABC' \\
    \overline{F'}   &= \overline{A'B'C + A'BC + AB'C + ABC'} \\
    F               &= (\overline{A'B'C}).(\overline{A'BC}).(\overline{AB'C}).(\overline{ABC'}) \\
                    &= (A+B+C').(A+B'+C').(A'+B+C').(A'+B'+C) \\
                    &= M_1.M_3.M_5.M_6 \\
                    &= \prod(1, 3, 5, 6)
\end{align*}
$$

We can also write the function directly from the truth table by taking the maxterms that are 0.
$$
\begin{align*}
    F   &= (A+B+C').(A+B'+C').(A'+B+C').(A'+B'+C) \\
        &= M_1.M_3.M_5.M_6 \\
        &= \prod(1, 3, 5, 6)
\end{align*}
$$


### Takeaways

From the above examples, we can see that the minterms and maxterms are complementary to each other. If a minterm is 1, then the corresponding maxterm is 0 and vice versa.

$$
\begin{array}{|ccc|c|}
\hline
\text{A} & \text{B} & \text{C} & \text{F} \\
\hline
0 & 0 & 0 & 1 \\
0 & 0 & 1 & 0 \\
0 & 1 & 0 & 1 \\
0 & 1 & 1 & 0 \\
1 & 0 & 0 & 1 \\
1 & 0 & 1 & 0 \\
1 & 1 & 0 & 0 \\
1 & 1 & 1 & 1 \\
\hline
\end{array}
$$

From the above truth table, the canonical SOP form is:
$$
F_1 = \sum(0, 2, 4, 7)
$$

Now the canonical POS form is:
$$
\begin{align*}
\overline{F_1} &= \sum(1, 3, 5, 6) \\
               &= m_1 + m_3 + m_5 + m_6
           F_2 &= \overline{m_1 + m_3 + m_5 + m_6} \\
               &= \overline{m_1}. \overline{m_3}. \overline{m_5}. \overline{m_6} \\
               &= M_1.M_3.M_5.M_6 \\
               &= \prod(1, 3, 5, 6)
\end{align*}
$$

Q. We are given the following boolean function:
$$
F(A,B,C) = \sum(1, 2, 5, 6)
$$

We can see that the function is in SOP form and it has 3 variables. So it has 8 minterms and 8 maxterms. In POS form, we will have the terms that are not present in the function. So the POS form of the function will be:
$$
\begin{align*}
F &= M_0.M_3.M_4.M_7 \\
  &= \prod(0, 3, 4, 7)
\end{align*}
$$


### Conversion from Non-Canonical to Canonical Form

Q. Given the boolean function:
$$
F(A, B) = A + B
$$
We can observe that the function is in non-canonical form. To convert it to canonical form, we have to utilize the boolean algebra postulates. The function can be written as:

$$
\begin{align*}
F &= A + B \\
    &= A.1 + B.1 \quad \text{Identity Law} \\
    &= A.(B+B') + B.(A+A') \quad \text{Complement Law} \\
    &= A.B + A.B' + A.B + A'.B \quad \text{Distributive Law} \\
    &= AB + AB' + A'B \\
\end{align*}
$$

Steps:

1. Include missing terms.
2. Expand the expression.
3. Remove redundant terms.

Q. Given the boolean function:
$$
F(A, B, C) = A + B.C + A.B
$$

We can see that the function is in non-canonical form. To convert it to canonical form, we have to utilize the boolean algebra postulates. 

Now for the given function:
$$
\text{For the first term:} \\
\begin{align*}
A &= A.1.1 \\
    &= A.(B+B').(C+C') \\
    &= (AB + AB').(C + C') \\
    &= ABC + ABC' + AB'C + AB'C' \\
\end{align*}

\text{For the second term:} \\
\begin{align*}
B.C &= B.C.1 \\
    &= B.C.(A+A') \\
    &= ABC + A'BC \\
\end{align*}

\text{For the third term:} \\
\begin{align*}
A.B &= A.B.1 \\
    &= A.B.(C+C') \\
    &= ABC + ABC' \\
\end{align*}
$$

So the function can be written as:
$$
\begin{align*}
F(A, B, C) &= ABC + AB'C + AB'C' + ABC + A'BC + ABC + ABC' \\
              &= ABC + ABC' + AB'C + AB'C' + A'BC \\
              &= \sum(3, 4, 5, 6, 7)
\end{align*}
$$

**Shortcut Method:**
$$
\begin{align*}
F(A, B, C)  &= A.B + C
            &= AB.X + XX.C \quad \text{X is a variable} \\
            &= 11.X + XX.1
\end{align*}
$$
For the value of X, 0 or 1 can be used. So values we get are:
$$110, 111$$, for $11.X$ 
$$001, 011, 101, 111$$, for $XX.1$
So the min-terms are:
$$
F = \sum(1, 3, 5, 6, 7)

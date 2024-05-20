# SOP & POS

## Minterm

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
A & B & C & \text{minterms} & \text{Notation} \\
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

### Example of Minterm

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


## Maxterm

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

### Example of Maxterm

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

## Why are they named Minters and Maxterms?

The prefix in Minterm 'min' suggests that it is the smallest term that can be formed from the variables. The prefix in Maxterm 'max' suggests that it is the largest term that can be formed from the variables.

## Takeaways

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
               &= m_1 + m_3 + m_5 + m_6 \\
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


## Conversion from Non-Canonical to Canonical Form

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

For the first term:
$$
\begin{align*}
A &= A.1.1 \\
    &= A.(B+B').(C+C') \\
    &= (AB + AB').(C + C') \\
    &= ABC + ABC' + AB'C + AB'C' \\
\end{align*}
$$
For the second term:
$$
\begin{align*}
B.C &= B.C.1 \\
    &= B.C.(A+A') \\
    &= ABC + A'BC \\
\end{align*}
$$

For the third term:
$$
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

Example:
$$
\begin{align*}
F   &= (A+B+C')(A'+C) \\
    &= (A+B+C')(A'+C+BB') \\
    &= (A+B+C')(A'+C+B)(A'+C+B') \\
\end{align*}
$$


**Shortcut Method:**
$$
\begin{align*}
F(A, B, C)  &= A.B + C \\
            &= AB.X + XX.C \quad \text{X is a variable} \\
            &= 11.X + XX.1
\end{align*}
$$
For the value of X, 0 or 1 can be used. So values we get are:
$$110, 111$$, for $$11.X$$ 
$$001, 011, 101, 111$$, for $$XX.1$$
So the min-terms are:
$$
F = \sum(1, 3, 5, 6, 7)
$$


## Sum of Products

It is used when the output is high.
Total number of combination is $$2^n$$, where n is the number of variables.

Truth Table:

$$
\begin{array}{|c|ccc|c|}
\hline
m & A & B & C & F \\
\hline
0 & 0 & 0 & 0 & 0 \\
1 & 0 & 0 & 1 & 0 \\
2 & 0 & 1 & 0 & 1 \\
3 & 0 & 1 & 1 & 0 \\
4 & 1 & 0 & 0 & 1 \\
5 & 1 & 0 & 1 & 1 \\
6 & 1 & 1 & 0 & 1 \\
7 & 1 & 1 & 1 & 1 \\
\hline
\end{array}
$$

Boolean Function of SOP,

$$
\begin{align*}
    F   &= A'.B.C' + A.B'.C' + A.B'.C + A.B.C' + A.B.C \\
\end{align*}
$$
In SOP form, _0 -> A', 1 -> A_.
This is known as standard or canonical SOP form. Because it is written directly from a truth table. In this form, each minterm has all the variables of the function in normal or complemented form.

$$
\begin{align*}
    F   &= A'.B.C' + A.B'.C' + A.B'.C + A.B.C' + A.B.C \\
        &= A'.B.C' + A.B'(C'+C) + A.B(C'+C) \\
        &= A'.B.C' + A.B' + A.B \\
        &= A'.B.C' + A(B'+B) \\
        &= A'.B.C' + A \\
        &= A'.B.C' + A.(B'+B) \\
        &= A'.B.C' + A \\
        &= A + B.C' \\
\end{align*}
$$

This is known as the minimal SOP form. Because it is written in the simplest form. In this form, each minterm does not have all the variables of the function in normal or complemented form.

$$
F(A,B,C)=m_2+m_4+m_5+m_6+m_7 \\
F(A,B,C)=\sum(2, 4, 5, 6, 7)
$$



## Product of Sums

It is used when the output is low.

Truth Table:

$$
\begin{array}{|c|ccc|c|}
\hline
M & A & B & C & F \\
\hline
0 & 0 & 0 & 0 & 0 \\
1 & 0 & 0 & 1 & 0 \\
2 & 0 & 1 & 0 & 0 \\
3 & 0 & 1 & 1 & 0 \\
4 & 1 & 0 & 0 & 1 \\
5 & 1 & 0 & 1 & 1 \\
6 & 1 & 1 & 0 & 1 \\
7 & 1 & 1 & 1 & 1 \\
\hline
\end{array}
$$

Boolean Function of POS,
$$
\begin{align*}
    Y = (A+B+C).(A+B+C').(A+B'+C).(A+B'+C') \\
\end{align*}
$$
In POS form, _0 -> A, 1 -> A'_. This is known as standard or canonical POS form. Because it is written directly from a truth table. In this form, each maxterm has all the variables of the function in normal or complemented form.


## Maths

**Q1:** Express $$F=X'Y + XZ$$ in POS form.

**Solution:**
$$
\begin{align*}
F   &= X'Y + XZ \\
    &= (X'Y + X)(X'Y + Z) \\
    &= (X+Y)(X+X').(Z+Y)(Z+X') \\
    &= (X+Y)(Y+Z)(Z+X') \\
\end{align*}
$$

Now,
$$
X+Y = X+Y+ZZ' = (X+Y+Z)(X+Y+Z') \\
Y+Z = Y+Z+XX' = (Y+Z+X)(Y+Z+X') \\
Z+X' = Z+X'+YY' = (Z+X'+Y)(Z+X'+Y') \\
$$

So,
$$
F = (X+Y+Z)(X+Y+Z')(X'+Y+Z)(X'+Y'+Z)
$$

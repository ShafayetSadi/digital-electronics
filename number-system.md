# Number System

## Decimal System

The decimal system is composed of 10 numerals or symbols. These 10 symbols are 0, 1, 2, 3, 4, 5, 6, 7, 8, 9; using these symbols as digits of a number, we can express any quantity. The decimal system, also called the base-10 system because it has 10 digits, has evolved naturally as a result of the fact that people have 10 fingers. In fact, the word digit is derived from the Latin word for "finger".

The decimal system is a positional-value system in which the value of a digit depends on its position.

## Binary System

In the binary system there are only two symbols or possible digit values, 0 and 1. Even so, this base-2 system can be used to represent any quantity that can be represented in decimal or other number systems. In general though, it will take a greater number of binary digits to express a given quantity.
Designing electronic circuits that operate with only two voltage levels is incredibly easy. That's why the binary number system is widely used as the foundation for almost every digital system. It offers simplicity and accuracy in its operations.

There are numerous devices that have only two operating states or can be operated in two extreme conditions.
Among these are: light bulb (bright or dark), diode (conducting or nonconducting), electromagnet (energized or de-energized), transistor (cut off or saturated), photocell (illuminated or dark), thermostat (open or closed), mechanical clutch (engaged or disengaged), and spot on a magnetic disk (magnetized or demagnetized)

## Conversion

TODO

$$
(3456)_{10} = 3*10^3 + 4*10^2 + 5*10^1 + 6*10^0 = 3000 + 400 + 50 + 6 \\
(11101010)_2 = 1*2^7 + 1*2^6 + 1*2^5 + 0*2^4 + 1*2^3 + 0*2^2 + 1*2^1 + 0*2^0 = 128 + 64 + 32 + 0 + 8 + 0 + 2 + 0 = 234
$$
The leftmost digit is the most significant digit (MSD) and the rightmost digit is the least significant digit (LSD).

## Arithmetic Operations

TODO

## 1's & 2's Complement

Up to now, we have been dealing with positive numbers. But in the binary system, we must also be able to represent negative numbers. There are two ways to represent negative numbers in binary: the 1's complement and the 2's complement.

For positive numbers, the MSB is 0. For negative numbers, the MSB is 1. The MSB is called the sign bit. The remaining bits are called the magnitude bits. This is called the signed-magnitude representation. But the signed-magnitude representation has a disadvantage. It has two representations for zero: +0 and -0. This makes arithmetic operations difficult.


### 1's Complement

The 1's complement of a binary number is obtained by changing all 1s to 0s and all 0s to 1s. It is also called the complement of the number. The 1's complement of a binary number is obtained by subtracting each digit of the number from 1. The 1's complement of a binary number is obtained by XORing each digit of the number with 1.

For positive numbers, the 1's complement is the same as the binary number. For negative numbers, the 1's complement is the complement of the binary number. The 1's complement of a binary number is obtained by changing the sign bit and taking the complement of the magnitude bits. But we still have two representations for zero: +0 and -0.

Whith `n` bits, the range of numbers that can be represented is from $-(2^{n-1}-1)$ to $2^{n-1}-1$.

### 2's Complement

The 2's complement of a binary number is obtained by adding 1 to the 1's complement of the number. The 2's complement of a binary number is obtained by XORing each digit of the number with 1 and adding 1 to the result. The 2's complement of a binary number is obtained by subtracting each digit of the number from 1 and adding 1 to the result.

For positive numbers, the 2's complement is the same as the binary number. For negative numbers, the 2's complement is the complement of the binary number. The 2's complement of a binary number is obtained by changing the sign bit and taking the complement of the magnitude bits and adding 1 to the result. In the 2's complement representation, there is only one representation for zero. So, arithmetic operations are easier in the 2's complement representation.

With `n` bits, the range of numbers that can be represented is from $-2^{n-1}$ to $2^{n-1}-1$.

## Arithmetic Operations in 2's Complement

TODO

## Why do we need binary number system?

* **Simplicity**: Binary system is simple and easy to understand. It has only two digits, 0 and 1.
* **Efficiency**: Binary system is efficient for digital systems. It is easy to implement in electronic circuits.
* **Compatibility**: Binary system is compatible with digital systems. It is used in computers, calculators, and other digital devices.
* **Ease of logic operations**: Binary system simplifies logic operations in digital systems. It is used in logic gates, flip-flops, and other digital components.
* **Error detection and correction**: Binary system is used in error detection and correction codes like Hamming codes and CRC (Cyclic Redundancy Check).
* **Universality and Standardization**: Binary system is universally used in digital systems. It is the standard for digital communication and data processing.

## Octal System

The octal system consists of 8 numerals or symbols: 0, 1, 2, 3, 4, 5, 6, and 7. It is commonly used in computer programming and is also referred to as the base-8 system because it has 8 digits. The octal system is a positional-value system, meaning that the value of a digit depends on its position.

We can see that $8=2^3$, indicating that each octal digit can be represented by 3 bits. The octal system is widely employed in computer programming because of its simplicity in converting between octal and binary. This means that each octal digit can be converted to 3 bits, and each set of 3 bits can be converted to an octal digit.

## Conversion of Octal

TODO

## Hexadecimal System

The hexadecimal system consists of 16 numerals or symbols: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, and F. It is commonly used in computer programming and is also referred to as the base-16 system because it has 16 digits. The hexadecimal system is a positional-value system, meaning that the value of a digit depends on its position.

We can see that $16=2^4$, indicating that each hexadecimal digit can be represented by 4 bits. It is widely employed in computer programming due to its simplicity in converting between hexadecimal and binary. This means that each hexadecimal digit can be converted to 4 bits, and each set of 4 bits can be converted to a hexadecimal digit.

## Conversion of Hexadecimal

TODO

## Floating Point Representation

Scientific notation is used to represent very large or very small numbers. In scientific notation, a number is expressed as the product of a mantissa and a power of 10. The mantissa is a number between 1 and 10, and the power of 10 indicates the position of the decimal point.

$$
(123.45)_{10} = 1.2345 * 10^2
\pm D.DDD \times 10^{\pm exponent}
$$

In binary, the mantissa is a number between 1 and 2, and the power of 2 indicates the position of the binary point.

$$
(101.11)_2 = 1.0111 * 2^2
\pm B.BBB \times 2^{\pm exponent}
$$

## Parity

It is a method of detecting errors in data transmission. A single bit error in a data stream can be detected by using a parity bit. The parity bit is added to the data before it is transmitted. It is an extra bit that makes the number of 1s either even or odd.

<figure><img src=".gitbook/assets/number-system/tx_rx.png" alt=""><figcaption><p>Data Transmission</p></figcaption></figure>

### Odd Parity

In odd parity, the number of 1s in the data is made odd by adding a parity bit. If the data has an even number of 1s, the parity bit is set to 1. If the data has an odd number of 1s, the parity bit is set to 0. The total number of 1s in the data and the parity bit is always `odd`. 

$$
\begin{array}{|c|c|c|c|c|c|c|c|c|c|c|}
\hline
\text{Data} &  & 1 & 1 & 0 & 1 & 0 & 1 & 1 & 1 & 0 \\
\hline
\text{With Parity} & 1 & 1 & 1 & 0 & 1 & 0 & 1 & 1 & 1 & 0 \\
\hline
\end{array}
$$

### Even Parity

In even parity, the number of 1s in the data is made even by adding a parity bit. If the data has an odd number of 1s, the parity bit is set to 1. If the data has an even number of 1s, the parity bit is set to 0. The total number of 1s in the data and the parity bit is always `even`. 

$$
\begin{array}{|c|c|c|c|c|c|c|c|c|c|c|}
\hline
\text{Data} & & 1 & 1 & 0 & 1 & 0 & 1 & 0 & 1 & 0 \\
\hline
\text{With Parity} & 1 & 1 & 1 & 0 & 1 & 0 & 1 & 0 & 1 & 0 \\
\hline
\end{array}
$$

Even parity code for in ASCII for the string "HELLO" is:
<figure><img src=".gitbook/assets/number-system/hello_parity.png" alt=""><figcaption><p>Even parity for 'HELLO'</p></figcaption></figure>

## Hamming Code

It is a method of error correction in data transmission. It is a block code that is capable of detecting up to two simultaneous bit errors and correcting single-bit errors.
It is named after its inventor, Richard Hamming. It is used in computer memory where it is known as ECC (error-correcting code). It is also used in satellite communication.
7-bit Hamming code is used commonly. In a 7-bit Hamming code, 4 bits are data bits and 3 bits are parity bits. The parity bits are placed at the positions of powers of 2.
The positions of parity bits are 1, 2, 4. The data bits are placed at the remaining positions. The positions of data bits are 3, 5, 6, 7. The parity bits are calculated by XORing the data bits at the positions of powers of 2. The data bits are calculated by XORing the data bits at the remaining positions. 

<figure><img src=".gitbook/assets/number-system/hamming-code.png" alt=""><figcaption><p>&-bit Hamming code</p></figcaption></figure>

$$
P_1 \rightarrow D_3,\ D_5,\ \ D_7 \\
P_2 \rightarrow D_3,\ D_6,\ D_7 \\
P_4 \rightarrow D_5,\ D_6,\ D_7 \\
$$

### Example

If the 7-bit Hamming code word received by the receiver is 1011011. Assuming that the data is transmitted using even parity, find whether the data is received correctly or not. If not, find the correct data.

**Solution:**
<figure><img src=".gitbook/assets/number-system/hamming-code.png" alt=""><figcaption><p>&-bit Hamming code</p></figcaption></figure>

$$
\begin{array}{|c|c|c|c|c|}
\hline
\text{Bit} & P_4 & D_5 & D_6 & D_7 \\
\hline
\text{Value} & 1 & 1 & 0 & 1\\
\hline
\end{array}
$$
As the value of $P_4$ is 1 and the total number of 1s in the data is odd, the data is not received correctly. So, $$P_4=1$$

$$
\begin{array}{|c|c|c|c|c|}
\hline
\text{Bit} & P_2 & D_3 & D_6 & D_7 \\
\hline
\text{Value} & 1 & 0 & 0 & 1\\
\hline
\end{array}
$$
As the value of $P_2$ is 1 and the total number of 1s in the data is even, the data is received correctly. So, $$P_2=0$$

$$
\begin{array}{|c|c|c|c|c|}
\hline
\text{Bit} & P_1 & D_3 & D_5 & D_7 \\
\hline
\text{Value} & 1 & 0 & 1 & 1\\
\hline
\end{array}
$$

As the value of $P_1$ is 1 and the total number of 1s in the data is odd, the data is not received correctly. So, $$P_1=1$$

So, $$ P_1=1,\ P_2=0,\ P_4=1 $$, which is the binary equivalent of 5. So, the position of the error is 5. The correct data is $$D_5=0$$.

The correct data is 
$$
D_3=0,\ D_5=0,\ D_6=0,\ D_7=1
$$
And the code word is 1001011.
<figure><img src=".gitbook/assets/number-system/hamming-example.png" alt=""><figcaption><p>Code word</p></figcaption></figure>

## 4-bit Even Parity Generator

$$
\begin{array}{|c|c|c|c|c|}
\hline
\ b_3 \ & \ b_2 \ & \ b_1 \ & \ b_0 \ & \ P_0 \ \\
\hline
0 & 0 & 0 & 0 & 0 \\
\hline
0 & 0 & 0 & 1 & 1 \\
\hline
0 & 0 & 1 & 0 & 1 \\
\hline
0 & 0 & 1 & 1 & 0 \\
\hline
0 & 1 & 0 & 0 & 1 \\
\hline
0 & 1 & 0 & 1 & 0 \\
\hline
0 & 1 & 1 & 0 & 0 \\
\hline
0 & 1 & 1 & 1 & 1 \\
\hline
1 & 0 & 0 & 0 & 1 \\
\hline
1 & 0 & 0 & 1 & 0 \\
\hline
1 & 0 & 1 & 0 & 0 \\
\hline
1 & 0 & 1 & 1 & 1 \\
\hline
1 & 1 & 0 & 0 & 0 \\
\hline
1 & 1 & 0 & 1 & 1 \\
\hline
1 & 1 & 1 & 0 & 1 \\
\hline
1 & 1 & 1 & 1 & 0 \\
\hline
\end{array}
$$

The K-map for the parity bit is:
<figure><img src=".gitbook/assets/number-system/parity-kmap.png" alt=""><figcaption><p>K-map for parity bit</p></figcaption></figure>

The Boolean expression for the parity bit is:
$$
P_0=b_0 \oplus b_1 \oplus b_2 \oplus b_3
$$

# Gray Code

Gray code is a binary code in which two successive numbers differ in only one bit. It is also known as the reflected binary code or unit distance code. The Gray code is a non-weighted code, which means that the weights associated with the bits in the code are not powers of 2. The Gray code is used in various applications, such as digital communications, error detection and correction, and data transmission.

**Characteristics of Gray Code:**

1. Each decimal digit is represented by a 4-bit binary code.
2. It is a non-weighted code.
3. Single-bit changes between consecutive numbers.
4. Reflection property: The Gray code of a number is the reflection of the Gray code of the previous number.

Let us see 4-bit Gray code for decimal numbers from 0 to 15.
$$
\begin{array}{|c|c|c|}
\hline
\text{Decimal} & \text{Binary} & \text{Gray} \\
\hline
0 & 0000 & 0000 \\
1 & 0001 & 0001 \\
2 & 0010 & 0011 \\
3 & 0011 & 0010 \\
4 & 0100 & 0110 \\
5 & 0101 & 0111 \\
6 & 0110 & 0101 \\
7 & 0111 & 0100 \\
8 & 1000 & 1100 \\
9 & 1001 & 1101 \\
10 & 1010 & 1111 \\
11 & 1011 & 1110 \\
12 & 1100 & 1010 \\
13 & 1101 & 1011 \\
14 & 1110 & 1001 \\
15 & 1111 & 1000 \\
\hline
\end{array}
$$

## Applications of Gray Code

### Linear Position Encoders

Linear position encoders are devices that are used to measure the position of an object along a linear path. These devices are used in various applications, such as robotics, automation, and machine tools. The linear position encoders use Gray code to represent the position of the object. The Gray code is used because it is less susceptible to errors during data transmission and provides accurate position information. The linear position encoders consist of a scale and a read head. The scale is a linear strip that is attached to the object whose position needs to be measured. The read head is a sensor that reads the position of the scale and converts it into a Gray code. The Gray code is then used to determine the position of the object. 

### Rotary Encoders

Rotary encoders are devices that are used to measure the angular position of an object. These devices are used in various applications, such as robotics, automation, and machine tools. The rotary encoders use Gray code to represent the angular position of the object. The Gray code is used because it is less susceptible to errors during data transmission and provides accurate position information. The rotary encoders consist of a disc and a read head. The disc is attached to the object whose angular position needs to be measured. The read head is a sensor that reads the position of the disc and converts it into a Gray code. The Gray code is then used to determine the angular position of the object. 

### Error Detection and Correction

Gray code is used in error detection and correction techniques. The Gray code is less susceptible to errors during data transmission, which makes it suitable for error detection and correction applications. The error detection and correction techniques use Gray code to detect and correct errors in data transmission. The error detection techniques use parity bits to detect errors in the data. The error correction techniques use Hamming codes to correct errors in the data. The error detection and correction techniques are used in various applications, such as digital communications, data transmission, and computer networks. They provide reliable and accurate data transmission, which is essential for the proper functioning of these systems.

## Binary to Gray Code Conversion

The conversion of binary code to Gray code can be done using the following steps:

1. Start from the leftmost bit of the binary code.
2. Copy the leftmost bit of the binary code to the Gray code.
3. XOR the leftmost bit with the next bit of the binary code.
4. Copy the result of the XOR operation to the Gray code.
5. Repeat steps 3 and 4 for the remaining bits of the binary code.

$$
\begin{align*}
(1010)_2 &= (1111)_G \\
G_3 &= B_3 \\
G_2 &= B_3 \oplus B_2 \\
G_1 &= B_2 \oplus B_1 \\
G_0 &= B_1 \oplus B_0
\end{align*}
$$

To convert Gray code to binary code, the following steps can be followed:

1. Start from the leftmost bit of the Gray code.
2. Copy the leftmost bit of the Gray code to the binary code.
3. XOR the rightmost bit of the binary with the next bit of the Gray code.
4. Copy the result of the XOR operation to the binary code.
5. Repeat steps 3 and 4 for the remaining bits of the Gray code.

$$
\begin{align*}
(1111)_G &= (1010)_2 \\
B_3 &= G_3 \\
B_2 &= B_3 \oplus G_2 \\
B_1 &= B_2 \oplus G_1 \\
B_0 &= B_1 \oplus G_0
\end{align*}
$$


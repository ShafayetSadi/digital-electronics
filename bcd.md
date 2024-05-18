# BCD

Binary Coded Decimal (BCD) is a type of binary code that represents a decimal number in a binary form. It is a way of representing each of the decimal digits with a binary code.
The most common BCD code is the 8421 code. The 8421 code is also known as the 4-bit BCD code. The 8421 code is a weighted code, which means that each bit in the code has a weight associated with it. The weights associated with the bits in the 8421 code are 8, 4, 2, and 1. 
There are other BCD codes as well, such as the 2421 code and the 5421 code. The 2421 code is a weighted code, with weights of 2, 4, 2, and 1. The 5421 code is a weighted code, with weights of 5, 4, 2, and 1.

Excess-3 and Gray codes are also examples of BCD codes. These are non-weighted codes, which means that the weights associated with the bits in the code are not powers of 2.

We also have Parity and Hamming codes. Parity codes are used to detect errors in data transmission. Hamming codes are used to correct errors in data transmission.

## 8421 BCD Code

The 8421 BCD code is a weighted code, with weights of 8, 4, 2, and 1. To convert decimal numbers to 8421 BCD code, we need to convert every decimal digit to its 4-bit binary equivalent.
$$
(23)_{10} = (0010 0011)_{BCD} \\
(56.79)_{10} = (0101 0110.0111 1001)_{BCD}
$$

## Why BCD is Used?

BCD is used in digital systems to represent decimal numbers in a binary form. It is used in applications where decimal numbers are required to be displayed or processed. BCD is used in digital clocks, calculators, and other devices that require decimal arithmetic.

* Each decimal digit is represented by a 4-bit binary code.
* It's fast and efficient.
* It's easy to convert between BCD and decimal.

## Why we need BCD?

* Accuracy in Calculations: BCD has no loss of precision in calculations because it represents each decimal digit separately.
* Ease of Human Understanding: BCD is easier for humans to read and understand as it directly represents decimal digits.
* Compatibility with Decimal Systems: BCD is compatible with decimal systems and can be easily converted to and from decimal.
* Simplified Arithmetic Operations: BCD simplifies arithmetic operations in digital systems, especially for applications involving decimal numbers.
* Error Detection and Correction: BCD codes like Excess-3 and Gray codes are used for error detection and correction in data transmission.

## Disadvantages of BCD

* Inefficient Use of Memory: BCD requires more memory to store decimal numbers compared to pure binary representation.
* Complex Conversion: Converting between BCD and binary or decimal can be more complex than working with pure binary numbers.
* Limited Range: BCD has a limited range of numbers that can be represented due to the 4-bit representation of each decimal digit.
* Complexity in Error Detection: While BCD codes like Excess-3 and Gray codes can be used for error detection, they add complexity to the system.

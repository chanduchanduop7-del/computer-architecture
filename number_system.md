



1. Number Systems ⭐⭐⭐
Binary, Decimal, Octal, Hexadecimal
Number conversions
1's and 2's complement
Signed and unsigned numbers
Binary arithmetic 
explain deeply about this

This is one of the most important topics in Computer Architecture, Digital Electronics, Embedded Systems, and C Programming. If you master Number Systems, learning microcontrollers, assembly language, memory addressing, and embedded programming becomes much easier.

1. Number Systems ⭐⭐⭐⭐⭐
A number system is a way to represent numbers using a set of symbols.

Computers understand only Binary (0 and 1) because electronic circuits have only two stable states:

OFF = 0

ON = 1

Humans use Decimal because we have 10 fingers.

There are four important number systems.

Number System	Base	Symbols
Decimal	10	0-9
Binary	2	0,1
Octal	8	0-7
Hexadecimal	16	0-9,A,B,C,D,E,F
Why Different Number Systems?
Suppose a binary number is

1111011010011010
Very difficult to read.

Instead we write

F69A
using hexadecimal.

Much easier.

That's why engineers use hexadecimal.

2. Decimal Number System (Base 10)
Uses

0 1 2 3 4 5 6 7 8 9
Example

548
Actually means

5×10² + 4×10¹ + 8×10⁰

=500+40+8

=548
Every digit position is a power of 10.

Binary Number System (Base 2)
Uses only

0
1
Example

101101
Expand it.

1×2⁵

0×2⁴

1×2³

1×2²

0×2¹

1×2⁰
Calculate

32 +0+8+4+0+1

=45
Therefore

101101₂ =45₁₀
Binary Place Values
Bit	7	6	5	4	3	2	1	0
Value	128	64	32	16	8	4	2	1
Example

11001010
128
64
0
0
8
0
2
0
Answer

128+64+8+2

=202
Octal Number System (Base 8)
Uses

0-7
Example

357₈
Expand

3×8²

5×8¹

7×8⁰

=192+40+7

=239
Hexadecimal Number System (Base 16)
Uses

0 1 2 3 4 5 6 7 8 9

A B C D E F
Where

A=10

B=11

C=12

D=13

E=14

F=15
Example

2AF₁₆
2×16²

A×16¹

F×16⁰

=2×256

+10×16

+15

=512+160+15

=687
Number Conversions ⭐⭐⭐⭐⭐
There are many types.

Decimal ↔ Binary

Binary ↔ Decimal

Binary ↔ Octal

Binary ↔ Hex

Decimal ↔ Hex

Decimal ↔ Octal
Let's learn all.

Decimal → Binary
Method

Repeatedly divide by 2.

Example

Convert

25
25÷2=12 remainder1

12÷2=6 remainder0

6÷2=3 remainder0

3÷2=1 remainder1

1÷2=0 remainder1
Read from bottom.

11001₂
Answer

25₁₀=11001₂
Another Example
Convert

50
50÷2=25 rem0

25÷2=12 rem1

12÷2=6 rem0

6÷2=3 rem0

3÷2=1 rem1

1÷2=0 rem1
Read upward.

110010₂
Binary → Decimal
Example

110101
1×32

1×16

0×8

1×4

0×2

1×1
32+16+4+1

=53
Binary → Octal
Rule

Group into 3 bits from right.

Example

101110111
101

110

111
Convert each group.

101=5

110=6

111=7
Answer

567₈
Octal → Binary
Replace every octal digit with 3 bits.

Example

572₈
5=101

7=111

2=010
Answer

101111010
Binary → Hexadecimal
Group into 4 bits.

Example

111010111001
1110

1011

1001
Convert

1110=E

1011=B

1001=9
Answer

EB9
Hex → Binary
Replace each hexadecimal digit by 4 bits.

Example

4AF
4=0100

A=1010

F=1111
Answer

010010101111
Decimal → Hexadecimal
Repeatedly divide by 16.

Example

350
350÷16=21 rem14(E)

21÷16=1 rem5

1÷16=0 rem1
Read upward.

15E
Hex → Decimal
Example

3B
3×16

+11

=48+11

=59
Binary Arithmetic ⭐⭐⭐⭐⭐
Same as decimal.

Only digits are

0
1
Binary Addition
Rules

0+0=0

0+1=1

1+0=1

1+1=10

1+1+1=11
Example

   1011

+  0110

-------
10001
Let's solve.

1+0=1

1+1=10

carry1

0+1+1=10

carry1

1+0+1=10

carry1

carry=1
Result

10001
Binary Subtraction
Rules

1-0=1

1-1=0

0-0=0

0-1

Borrow
Example

1010

-0011

=0111
Binary Multiplication
Rules

0×0=0

1×0=0

1×1=1
Example

101

×11

------

101

1010

------

1111
Decimal check

5×3=15
Binary

1111
Correct.

Binary Division
Same as decimal long division.

Example

1100÷10
Decimal

12÷2=6
Binary

110
Signed and Unsigned Numbers ⭐⭐⭐⭐⭐
Computers store data in bits.

Consider

8 bits
00000000

to

11111111
There are 256 combinations.

These can be interpreted in two ways.

Unsigned Numbers
Only positive numbers.

Range

0

to

255
Formula

0

to

2ⁿ−1
where

n = number of bits
Example

8-bit

0

to

255
16-bit

0

to

65535
Signed Numbers
Need both

Positive

Negative
Usually stored using Two's Complement.

Range

-128

to

+127
for 8 bits.

Formula

−2ⁿ⁻¹

to

2ⁿ⁻¹−1
Example

8 bits

−128

to

127
MSB (Most Significant Bit)
The leftmost bit.

Example

10010110
The first bit is the MSB.

In signed numbers:

MSB = 0 → Positive

MSB = 1 → Negative

LSB (Least Significant Bit)
The rightmost bit.

Example

10010110
The last bit is the LSB.

1's Complement ⭐⭐⭐⭐
Definition

Invert every bit.

0→1

1→0
Example

Original

00110110
Invert

11001001
That is the 1's complement.

2's Complement ⭐⭐⭐⭐⭐
Most computers represent negative integers using two's complement because arithmetic becomes much simpler.

Steps:

Find the 1's complement (invert all bits).

Add 1 to the result.

Example: Find the 2's complement of

00110110
Step 1 (1's complement):

11001001
Step 2 (add 1):

11001010
Answer:

11001010
Representing Negative Numbers
Represent -5 using 8 bits.

Start with +5:

00000101
Take the 1's complement:

11111010
Add 1:

11111011
So:

-5 = 11111011
Why Use 2's Complement?
Suppose we calculate:

5 + (-5)
Binary:

00000101

+

11111011

------------

1 00000000
The carry beyond 8 bits is discarded, leaving:

00000000
which is 0. This makes addition and subtraction work with the same hardware, which is why CPUs use two's complement.


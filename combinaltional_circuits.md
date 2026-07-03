



4. Combinational Circuits ⭐⭐⭐
Half Adder
Full Adder
Half Subtractor
Full Subtractor
Multiplexer (MUX)
Demultiplexer (DEMUX)
Encoder
Decoder
Comparator

4. Combinational Circuits ⭐⭐⭐
Complete Guide for Computer Architecture & Embedded Systems
What are Combinational Circuits?
A combinational circuit is a digital circuit whose output depends only on the current inputs.

There is no memory and no feedback.

Output = f(Current Inputs)

Unlike sequential circuits, combinational circuits do not remember previous inputs.

Characteristics
No memory element

No clock signal required

No feedback path

Output changes immediately when inputs change

Built using logic gates

Inputs
   │
   ▼
Logic Gates
   │
   ▼
Outputs
Difference Between Combinational and Sequential Circuits
Combinational Circuit	Sequential Circuit
No memory	Has memory
Output depends on current input	Output depends on current input + previous state
No clock required	Clock required
Faster	Comparatively slower
Examples: Adders, MUX	Flip-Flops, Registers, Counters
Applications
Used almost everywhere inside a CPU.

Examples:

ALU

Arithmetic Unit

Address Decoder

Memory Selection

Data Routing

Digital Comparator

Instruction Decoder

1. Half Adder
A Half Adder adds two binary bits.

A + B
It produces

Sum

Carry

Block Diagram
A ----\
       > Half Adder ---- Sum
B ----/               \
                     Carry
Truth Table
A	B	Sum	Carry
0	0	0	0
0	1	1	0
1	0	1	0
1	1	0	1
Boolean Equation
Sum
S = A ⊕ B
(XOR Gate)

Carry
C = A · B
(AND Gate)

Circuit
A ---- XOR ---- Sum
 \
  \
   AND ---- Carry
  /
 /
B
Example
A = 1
B = 1

1 + 1 = 10

Sum = 0
Carry = 1
Limitation
Cannot add previous carry.

Therefore Half Adder is not enough for multi-bit addition.

2. Full Adder
A Full Adder adds

A
B
Carry-in (Cin)
Outputs

Sum
Carry-out
Block Diagram
A
 \
  \
   Full Adder ---- Sum
  /
 /
B

Cin -----------/
Truth Table
A	B	Cin	Sum	Carry
0	0	0	0	0
0	0	1	1	0
0	1	0	1	0
0	1	1	0	1
1	0	0	1	0
1	0	1	0	1
1	1	0	0	1
1	1	1	1	1
Boolean Equation
Sum
S = A ⊕ B ⊕ Cin
Carry
Cout = AB + BCin + ACin
Construction
A Full Adder is made using

2 Half Adders
+
1 OR Gate
Half Adder
      \
       OR → Carry
Half Adder
Example
A = 1
B = 1
Cin = 1

1 + 1 + 1 = 11

Sum = 1
Carry = 1
Applications
CPU Arithmetic Logic Unit

Binary Addition

Processors

Calculators

Half Adder vs Full Adder
Half Adder	Full Adder
2 Inputs	3 Inputs
No Carry Input	Carry Input Available
Simpler	More Complex
Single-bit Addition	Multi-bit Addition
3. Half Subtractor
Performs subtraction

A − B
Outputs

Difference

Borrow

Truth Table
A	B	Difference	Borrow
0	0	0	0
0	1	1	1
1	0	1	0
1	1	0	0
Boolean Equation
Difference

D = A ⊕ B
Borrow

Borrow = A'B
Example
0 − 1

Difference = 1
Borrow = 1
(Binary result: -1 represented using borrow.)

4. Full Subtractor
Subtracts

A − B − Borrow_in
Outputs

Difference

Borrow Out

Truth Table
A	B	Bin	Difference	Borrow
0	0	0	0	0
0	0	1	1	1
0	1	0	1	1
0	1	1	0	1
1	0	0	1	0
1	0	1	0	0
1	1	0	0	0
1	1	1	1	1
Difference Equation
D = A ⊕ B ⊕ Bin
Borrow Equation
Borrow = A'B + A'Bin + BBin
Applications
Binary subtraction

ALU

Digital calculators

5. Multiplexer (MUX)
A Multiplexer is a Many-to-One data selector.

It selects one input and forwards it to the output based on the select lines.

Many Inputs
      ↓
     MUX
      ↓
 One Output
2:1 Multiplexer
Inputs

I0
I1
Select

S
Output

Y
Block
I0 ----\
         \
          MUX ---- Y
         /
I1 ----/

      S
Truth Table
S	Output
0	I0
1	I1
Boolean Equation
Y = S'I0 + SI1
Example
I0 = 5V
I1 = 0V

S = 0

Output = 5V
Types
2:1

4:1

8:1

16:1

Applications
Data Selection

CPU Data Bus

Communication Systems

Memory Selection

6. Demultiplexer (DEMUX)
A DEMUX is One-to-Many.

One Input
     ↓
   DEMUX
     ↓
Many Outputs
1:2 DEMUX
Input = D

Select = S

Outputs

Y0
Y1
Truth Table
S	Y0	Y1
0	D	0
1	0	D
Applications
Data Distribution

Memory Systems

Communication

Display Control

MUX vs DEMUX
MUX	DEMUX
Many → One	One → Many
Selects one input	Routes one input
Data Selector	Data Distributor
7. Encoder
An Encoder converts

Many Inputs
↓

Binary Code
Example

8 Inputs

↓

3-bit Output
4:2 Encoder
Inputs

D0
D1
D2
D3
Outputs

A
B
Truth Table
Input Active	AB
D0	00
D1	01
D2	10
D3	11
Applications
Keyboard Encoding

Interrupt Handling

Data Compression

Communication

Priority Encoder
If multiple inputs become HIGH,

Priority Encoder chooses

Highest Priority Input
Used in

CPU Interrupts

Controllers

Embedded Systems

8. Decoder
A Decoder performs the opposite operation.

Binary Input

↓

One Active Output
2:4 Decoder
Inputs

A
B
Outputs

Y0
Y1
Y2
Y3
Truth Table
AB	Active Output
00	Y0
01	Y1
10	Y2
11	Y3
Applications
Memory Address Decoding

Seven Segment Display

CPU Instruction Decoding

Chip Selection

Encoder vs Decoder
Encoder	Decoder
Many → Binary	Binary → Many
Compression	Expansion
Input Reduction	Output Selection
9. Comparator
A Comparator compares two binary numbers.

Outputs

A > B

A = B

A < B
Example
A = 1010

B = 1001

Result

A > B
1-Bit Comparator Truth Table
A	B	A>B	A=B	A<B
0	0	0	1	0
0	1	0	0	1
1	0	1	0	0
1	1	0	1	0
Applications
CPU Comparison Instructions

Sorting Algorithms (Hardware)

Digital Measurement Systems

Password Verification

Address Comparison

Real-Life CPU Example
Suppose the processor executes:

if (A > B)
The hardware comparator compares:

Register A

with

Register B
If:

A > B
then the CPU sets the Greater Than flag, allowing the program to branch to the appropriate instruction.

Combinational Circuits Inside a CPU
                 CPU
                  │
      ┌───────────┴───────────┐
      │                       │
    Decoder               Comparator
      │                       │
      ├──────────┐            │
      │          │            │
    MUX        DEMUX          │
      │          │            │
      └──────┬───┘            │
             │                │
          Full Adder      Full Subtractor
             │
            ALU
Quick Revision Table
Circuit	Inputs	Outputs	Primary Function
Half Adder	2	Sum, Carry	Adds two bits
Full Adder	3	Sum, Carry	Adds two bits with carry-in
Half Subtractor	2	Difference, Borrow	Subtracts two bits
Full Subtractor	3	Difference, Borrow	Subtracts with borrow-in
Multiplexer (MUX)	Many + Select	1	Selects one input
Demultiplexer (DEMUX)	1 + Select	Many	Routes one input to one output
Encoder	Many	Binary Code	Converts active input to binary
Decoder	Binary	Many	Activates one output from binary input
Comparator	Two Binary Numbers	A>B, A=B, A<B	Compares values
Interview Questions
Basic
What is a combinational circuit?

How does a combinational circuit differ from a sequential circuit?

Why do combinational circuits not require a clock?

Adders & Subtractors
Explain the working of a Half Adder with a truth table.

Why can't a Half Adder be used for multi-bit addition?

Derive the Boolean expressions for a Full Adder.

What is the purpose of the Carry-in input in a Full Adder?

Explain the difference between a Half Subtractor and a Full Subtractor.

Multiplexer & Demultiplexer
What is a Multiplexer? Explain the operation of a 4:1 MUX.

Write the Boolean expression for a 2:1 MUX.

What is the difference between a MUX and a DEMUX?

Give two practical applications of a DEMUX.

Encoder & Decoder
What is the difference between an Encoder and a Decoder?

What is a Priority Encoder, and why is it needed?

Explain the operation of a 2:4 Decoder with its truth table.

How are decoders used in memory address decoding?

Comparator
What is the function of a digital comparator?

Explain the outputs of a 1-bit comparator.

How are comparators used in CPUs and ALUs?

Advanced
How is a Full Adder constructed using two Half Adders and an OR gate?

Explain how combinational circuits are used inside the Arithmetic Logic Unit (ALU).

Compare Adders, Multiplexers, Decoders, and Comparators in terms of functionality and applications.

Design a 4-bit ripple-carry adder using Full Adders.

Explain the role of combinational circuits in instruction execution within a processor.

This covers the complete set of fundamental combinational circuits required for Computer Architecture, Digital Electronics, Embedded Systems, technical interviews, and university examinations.



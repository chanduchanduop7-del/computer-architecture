



2. Logic Gates ⭐⭐⭐
AND
OR
NOT
NAND
NOR
XOR
XNOR
Truth tables
Universal gates

Logic Gates (⭐⭐⭐) – Complete Guide for Embedded Systems
Logic gates are the building blocks of digital electronics. Every microcontroller, CPU, RAM, ALU, FPGA, and digital circuit is made using millions or billions of logic gates.

In embedded systems, sensors usually provide 0 or 1 (LOW or HIGH), and the microcontroller makes decisions using logic gates.

1. What is Digital Logic?
Digital electronics understands only two values:

Binary	Voltage (Typical)	Meaning
0	0V	LOW / OFF / FALSE
1	5V or 3.3V	HIGH / ON / TRUE
Example:

A Push Button

Not Pressed → 0

Pressed → 1

LED

OFF → 0

ON → 1

2. What is a Logic Gate?
A logic gate is an electronic circuit that performs a logical operation.

Think of it like a decision-maker.

Example

Input A = 1

Input B = 0

The logic gate decides the output according to its rule.

3. AND Gate
Symbol
A ----\
       )---- Output
B ----/
Rule
Output is HIGH only when ALL inputs are HIGH.

Boolean Expression
Y = A · B
or

Y = AB
Truth Table
A	B	Output
0	0	0
0	1	0
1	0	0
1	1	1
Example
Door opens only if

Password Correct = 1

Fingerprint Correct = 1

Password AND Fingerprint
Both must be true.

Embedded Example
Turn ON motor only if

Temperature High
AND
Water Available
Both conditions must be satisfied.

4. OR Gate
Symbol
A ----\
       )≥1---- Output
B ----/
Rule
Output is HIGH if ANY input is HIGH.

Boolean Equation
Y = A + B
Truth Table
A	B	Output
0	0	0
0	1	1
1	0	1
1	1	1
Example
Alarm activates if

Smoke detected

OR

Gas detected

Either one is enough.

Embedded Example
Fan ON if

Temperature High
OR
Manual Switch ON
5. NOT Gate
Symbol
A ----|>o---- Output
Small bubble means inversion.

Rule
Reverses the input.

Boolean Equation
Y = A'
or

Y = NOT A
Truth Table
A	Output
0	1
1	0
Example
Button released

0
NOT gate makes it

1
Embedded Example
Many sensors are Active LOW.

Example

Sensor detects obstacle

Output = 0

NOT gate converts it into

1
6. NAND Gate
NAND = NOT AND

Symbol
A ----\
       )o---- Output
B ----/
Bubble means NOT.

Equation
Y = (AB)'
Truth Table
A	B	Output
0	0	1
0	1	1
1	0	1
1	1	0
Rule
Everything same as AND

Except final answer is inverted.

Example
1 AND 1 = 1

NOT 1 = 0
Why NAND is Important?
NAND is called a Universal Gate.

Because using only NAND gates we can build

AND

OR

NOT

XOR

CPU

Memory

Microcontroller

Entire processors are built mainly using NAND gates.

7. NOR Gate
NOR = NOT OR

Equation
Y = (A+B)'
Truth Table
A	B	Output
0	0	1
0	1	0
1	0	0
1	1	0
Rule
Everything same as OR

Invert the answer.

Why NOR is Important?
NOR is also a Universal Gate.

Using only NOR gates we can build every digital circuit.

8. XOR Gate (Exclusive OR)
This gate checks whether inputs are DIFFERENT.

Equation
Y = A ⊕ B
Truth Table
A	B	Output
0	0	0
0	1	1
1	0	1
1	1	0
Rule
Output HIGH only when inputs are different.

Example
A=1
B=0

Different?

Yes

Output =1
Real Example
Two switches controlling one light.

Light changes whenever only one switch changes.

Embedded Example
Error detection

Parity bits

Binary addition

9. XNOR Gate
XNOR = NOT XOR

Equation
Y = (A⊕B)'
Truth Table
A	B	Output
0	0	1
0	1	0
1	0	0
1	1	1
Rule
Output HIGH when inputs are SAME.

Example
Password checking

Entered Password

Stored Password

If same

Output = 1

Complete Truth Table
A	B	AND	OR	NAND	NOR	XOR	XNOR
0	0	0	0	1	1	0	1
0	1	0	1	1	0	1	0
1	0	0	1	1	0	1	0
1	1	1	1	0	0	0	1
NOT Gate

A	NOT
0	1
1	0
Universal Gates
A universal gate is a gate that can implement any Boolean function or construct all other logic gates by itself.

There are only two universal gates:

NAND

NOR

Constructing Other Gates Using NAND
NOT Gate
Connect both inputs together:

A ----\
       )o---- Y
A ----/
Output:

Y = (A · A)' = A'
AND Gate
Use two NAND gates:

A ----\
       )o----\
B ----/      \
              )o---- Y
             /
            (inputs tied together)
OR Gate
Using De Morgan's Law:

A' NAND B' = A + B
Constructing Other Gates Using NOR
NOT Gate
Tie both inputs together:

Y = (A + A)' = A'
OR Gate
Use two NOR gates (first NOR, then invert).

AND Gate
Using De Morgan's Law:

(A' + B')' = AB
De Morgan's Theorems
These are very important for simplifying digital circuits.

First Theorem
(A · B)' = A' + B'
Meaning: NOT of AND = OR of NOTs

Second Theorem
(A + B)' = A' · B'
Meaning: NOT of OR = AND of NOTs

Boolean Algebra Basics
Some common identities:

Law	Expression
Identity	A + 0 = A
Identity	A · 1 = A
Null	A + 1 = 1
Null	A · 0 = 0
Idempotent	A + A = A
Idempotent	A · A = A
Complement	A + A' = 1
Complement	A · A' = 0
Double Negation	(A')' = A
These rules are used to simplify logic expressions and design efficient circuits.

Applications in Embedded Systems
AND: Turn on a motor only if two safety conditions are met.

OR: Trigger an alarm if either smoke or gas is detected.

NOT: Invert active-low sensor signals.

NAND/NOR: Internal building blocks of CPUs, memory chips, and microcontrollers.

XOR: Parity generation, error detection, binary addition, and encryption.

XNOR: Equality checking, password verification, and digital comparators.

Interview Questions
Which gate is known as the universal gate?

NAND and NOR

Why is XOR called "Exclusive OR"?

Because the output is HIGH only when the inputs are different.

What is the output of an AND gate when one input is 0?

0

Which gate is used for equality comparison?

XNOR

What is the output of a NOT gate if the input is 1?

0

State De Morgan's Theorems.

(
A
⋅
B
)
′
=
A
′
+
B
′
(A⋅B) 
′
 =A 
′
 +B 
′
 

(
A
+
B
)
′
=
A
′
⋅
B
′
(A+B) 
′
 =A 
′
 ⋅B 
′
 

Key Points to Remember
AND → All inputs must be HIGH.

OR → At least one input must be HIGH.

NOT → Inverts the input.

NAND → AND followed by NOT (Universal Gate).

NOR → OR followed by NOT (Universal Gate).

XOR → HIGH when inputs are different.

XNOR → HIGH when inputs are the same.

NAND and NOR alone can build any digital circuit. These concepts form the foundation of processors, memory, microcontrollers, and embedded system hardware.





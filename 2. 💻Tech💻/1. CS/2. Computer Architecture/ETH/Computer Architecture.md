# Abstraction
![[Pasted image 20230129203849.png]]

The critical technique for managing complexity is abstraction: hiding details when they are not important.

Discipline is the act of intentionally restricting your design choices so that you can work more productively at a higher level of abstraction.

- Hierarchy involves dividing a system into modules, then further subdi-  
viding each of these modules until the pieces are easy to understand.  
- Modularity states that the modules have well-defined functions and  
interfaces, so that they connect together easily without unanticipated  
side effects.  
- Regularity seeks uniformity among the modules. Common modules  
are reused many times, reducing the number of distinct modules that  
must be designed.


The amount of information D in a discrete valued variable with N distinct states is measured in units of bits as
![[Pasted image 20230129204115.png]]

# Binary Numbers
A group of eight bits is called a byte. It represents one of 2^8 = 256 possibilities.

A group of four bits, or half a byte, is called a nibble. It represents one of 2^24 = 16 possibilities

Microprocessors handle data in chunks called words
- Architecture, some 32 bit others 64 bit

- Addition
![[Pasted image 20230129204354.png]]
the bit that is carried over to the neighboring column is called the carry bit
## Two’s Complement Numbers
Two’s complement numbers are identical to unsigned binary numbers except that the most significant bit position has a weight of -2^N-1 instead of 2^N-1

In two’s complement representation, zero is written as all zeros: 00...0002. The most positive number has a 0 in the most significant position and 1’s elsewhere: 01...1112 = 2^N-1 - 1. The most negative number has a 1 in the most significant position and 0’s elsewhere: 10...0002 = -2^N-1. And -1 is written as all ones: 11...111.

The sign of a two’s complement number is reversed in a processcalled taking the two’s complement. The process consists of inverting allof the bits in the number, then adding 1 to the least significant bitposition. This is useful to find the representation of a negative numberor to determine the magnitude of a negative number.

# Logic Gate
## NOT
![[Pasted image 20230129204803.png]]
The NOT gate’s output is the inverse of its input
## BUFFER
![[Pasted image 20230129204831.png]]
It simply copies the input to the output
## AND
![[Pasted image 20230129204859.png]]
The AND gate produces a TRUE output, Y, if and only if both A and B are TRUE
## OR
![[Pasted image 20230129204924.png]]
The OR gate shown in Figure 1.15 produces a TRUE output, Y, if either A or B (or both) are TRUE
## XOR
![[Pasted image 20230129204952.png]]
XOR (exclusive OR, pronounced “ex-OR”) is TRUE if A or B, but not both, are TRUE
## NAND
![[Pasted image 20230129205007.png]]
Not and. Its output is TRUE unless both inputs are TRUE.
## NOR
![[Pasted image 20230129205047.png]]
The NOR gate performs NOT OR. Its output is TRUE if neither A nor B is TRUE

## XNOR
![[Pasted image 20230129205131.png]]
The two-input XNOR gate is sometimes called an **equality gate** because its output is TRUE when the inputs are equal.

# DIGITAL ABSTRACTION
The mapping of a continuous variable onto a discrete binary variable isdone by defining logic levels, as shown in Figure 1.23. The first gate iscalled the driver and the second gate is called the receiver
![[Pasted image 20230129205240.png]]

The driver produces a  
LOW (0) output in the range of 0 to VOL or a HIGH (1) output in the  
range of VOH to VDD. If the receiver gets an input in the range of 0 to  
VIL, it will consider the input to be LOW. If the receiver gets an input in  
the range of VIH to VDD, it will consider the input to be HIGH. If, for  
some reason such as noise or faulty components, the receiver’s input  
should fall in the forbidden zone between VIL and VIH, the behavior of  
the gate is unpredictable.
![[Pasted image 20230129205313.png]]

To avoid inputs falling into the forbidden zone, digital logic gates are  
designed to conform to the static discipline. The static discipline requires  
that, given logically valid inputs, every circuit element will produce logi-  
cally valid outputs.
![[Pasted image 20230129205418.png]]

# CMOS Transistor
## Transistor types
Transistors are electrically controlled switches that turn ON or OFF when a voltage or current is applied to a control terminal.
The two main types of transis-  tors are bipolar transistors and metal-oxide-semiconductor field effect  transistors (MOSFETs or MOS transistors, pronounced “moss-fets" or M-O-S”, respectively)

## MOSFET
A MOSFET is a sandwich of several layers of conducting and insulating materials. MOSFETs are built on thin flat wafers of silicon of about 15 to 30 cm in diameter. The manufacturing process begins with a bare wafer. The process involves a sequence of steps in which dopants are implanted into the silicon, thin films of silicon dioxide and silicon are grown, and metal is deposited.

# Circuit
![[Pasted image 20230130204305.png]]
a circuit is a network that processes discretevalued variables.

- one or more discrete-valued input terminals
- one or more discrete-valued output terminals
- a **functional specification** describing the relationship between inputs and outputs
- a **timing specification** describing the delay between inputs changing and outputs responding.

An element is itself a circuit with inputs, outputs, and a specification
A node is a wire, whose voltage conveys a discrete-valued variable

- combinational
	- A combinational circuit’s outputs depend only on the **current values of the inputs**; in other words, it combines the current input values to compute the output.
	- **memoryless**
- sequential
	- A sequential circuit’s outputs depend on both **current and previous values of the inputs**; in other words, it depends on the input sequence
	- has **memory**

![[Pasted image 20230130205320.png]]
![[Pasted image 20230130205316.png]]
To simplify drawings, we often use a single line with a slash through it and a number next to it to indicate a bus, a bundle of multiple signals

- combinational compostition
	- **Every circuit element is itself combinational.**
	- Every node of the circuit is either designated **as an input to the circuit or connects to exactly one output terminal of a circuit element.**
	- The circuit contains **no cyclic paths**: every path through the circuit visits each circuit node at most once.

# Boolean 
## Equation
In Boolean equations, NOT has the highest precedence, followed by AND(product), then OR(sum). Just as in ordinary equations, products are performed before sums

## Algebra
Boolean algebra is based on a set of axioms that we assume are correct. Axioms are unprovable in the sense that a definition cannot be proved

# Logic to Gates
![[Pasted image 20230130212443.png]]
- Inputs are on the left (or top) side of a schematic.
- Outputs are on the right (or bottom) side of a schematic.
- Whenever possible, gates should flow from left to right
- Straight wires are better to use than wires with multiple corners (jagged wires waste mental effort following the wire rather than thinking of what the circuit does).
![[Pasted image 20230130212627.png]]
- Wires always connect at a T junction.
- A dot where wires cross indicates a connection between the wires.
- Wires crossing without a dot make no connection.

# K-Map(Karnaugh Maps)
![[Pasted image 20230131200019.png]]
![[Pasted image 20230131200209.png]]
Rules for finding a minimized equation from a K-map
- Use the fewest circles necessary to cover all the 1’s.
- All the squares in each circle must contain 1’s.
- Each circle must span a rectangular block that is a power of 2 (i.e., 1, 2, or 4) squares in each direction.
- Each circle should be as large as possible
- A circle may wrap around the edges of the K-map.
- A 1 in a K-map may be circled multiple times if doing so allows fewer circles to be used.
- We only write the Viriable that is not changing[22:30](https://www.youtube.com/watch?v=FPrcIhqNPVo)
![[Pasted image 20230131201451.png]]
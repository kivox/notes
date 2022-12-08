---
{"dg-publish":true,"permalink":"/computer-science/cpu/components-of-a-cpu/","dgHomeLink":true,"dgPassFrontmatter":false}
---


# Components of a CPU
-   MAR
	- holds the address of the current instruction that is to be fetched from memory, or the address in memory to which data is to be transferred.
- MBR
	- Memory buffer register
	- Holds the contents found at the address held in the MAR, or data which is to be transferred to main memory.
-   MDR
	- Memory Data Register
-   CIR
	- Current Instruction Register
	- Holds the instruction that is currently being decoded and executed.
-   PC
	- Program Counter
	    - Holds the memory address of the next instruction to be fetched from main memory.
-   ALU
	- Arithmetic Logic Unit
	- A register used by the arithmetic logic unit (ALU) to store the results of calculations.
-   Accumulator
	- Holds the data being processed and the results of processing.
-   Cache
	- A piece of temporary memory. It can refer to a part of the RAM, storage disk, CPU, or an area for storing web pages.
-   Status register
	- The status register is a hardware register that contains information about the state of the processor.
-   Control unit
	- The component of the CPU that manages instructions.
-   Assembly language
	- An assembly language is a type of low-level programming language that is intended to communicate directly with a computer's hardware. Unlike machine language, which consists of binary and hexadecimal characters, assembly languages are designed to be readable by humans.
-   Opcodes
	- An opcode is the portion of a machine language instruction that specifies the operation to be performed. Beside the opcode itself, most instructions also specify the data they will process, in the form of operands.
-   Operands
	- An operand is the object of a mathematical operation, i.e., it is the object or quantity that is operated on.
	- \+ \- \/ \*

-   Relationship between machine code and assembly language
	- Assembly language is a low-level programming language . It equates to machine code but is more readable. It can be directly translated into machine code, but it uses mnemonics to represent the instructions to make it easier to understand.
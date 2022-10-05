---
{"dg-publish":true,"permalink":"/computer-science/io-and-storage-devices/ram-rom-and-storage/","dgHomeLink":true,"dgPassFrontmatter":false}
---

# RAM, ROM & Storage
- # RAM
	- RAM is considered primary memory, it is fast and direct, it is directly accessed by the CPU. It acts as a temporary store for program instructions and program data. It can only store things temporarily as it is volatile, volatile means it loses all data when powered off.
	- Data stored in RAM is volatile, meaning nothing permeant should be stored on them. 
	- Instructions are stored in RAM for the CPU to later access them, this can be instructions but also  program data such as configs that don't need to be read from secondary storage.
	- RAM is also often used as a caching layer, this is if the CPU's cache is full.
	- ### How does the CPU execute instructions?
		- The CPU is constantly fetching instructions from RAM, it gets an address from it's address register then fetches it from RAM, then executes it and in some cases returns data to store in another address on the RAM.

- # ROM
- ROM stands for Read-Only Memory. ROM usually stores the BIOS of a system, and in some cases the operating system - this is only the case for very old computers.
- As its name suggests, ROM can only be read from. Data and Instructions on it are written while the chip is getting manufactured.
- These chips are almost always embedded on the system's motherboard.
- Always used in computers, most commonly used in embedded systems.

- # Storage
	- This is permeant storage. When power goes out, the data stored on these devices stays in tacked.
	- This is known as secondary storage.
	- It is sometimes used as RAM, when the RAM is very full a portion of one of these drives is allocated, called virtual memory.
	- Virtual Memory is very slow, so it should be avoided when possible.

| Storage | Type | Speed | Capacity | Relative Cost (on release) |
| --- | --- | --- | --- | --- |
| Floppy Disk | Magnetic | Slow | Lowest | High |
| Solid State | Solid State | v.Fast | High | Affordable |
| Hard Disk   | Magnetic | Fast | High | v.Affordable |
| USBs & SD Cards   | Flash | Slow | Low | Highest |
| CDs & DVDs | Optical | Slow | Low | Low |

- # Storage Types:
	- ### Optical:
	- ### Magnetic:
	- ### Solid State:
	- ### Virtual (Cloud Storage):
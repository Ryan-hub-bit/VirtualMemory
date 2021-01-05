# VirtualMemory

Three memory problems:

- Not enough RAM
- Holes in our address space
- Programs writing over each other

#### what is virtual memory?

- indirection
- how does it solve the problems?
- Page Tables and Translation





### What if we don't have enough  memory? 

MIPS gives each program its own 32-bit address space

Programs can access any byte in their 32-bit address space

if a 32-bite program run on a  30-bit RAM (1GB), it will crash if e try to access more than 1GB

#### 

### Holes  in our address space

How do programs share the memory? 

![Screen Shot 2021-01-05 at 5.00.08 AM](/Users/liukun/Documents/Screen/Screen Shot 2021-01-05 at 5.00.08 AM.png)



**WE give each program it's own virtual memory space**

Separately map each program's memory space to the RAM memory space. Mapping gives us flexibility in how we use the physical RAM memory.



What is virtual memory (VM) ? 

Virtual memory is a layer of indirection(间接).

Without Virtual Memory: Program address = RAM Address, No VM: the system will crash if we try to access more RAM than we have.

Virtual memory takes program addresses and maps them to RAM addresses

![Screen Shot 2021-01-05 at 5.15.11 AM](/Users/liukun/Documents/Screen/Screen Shot 2021-01-05 at 5.15.11 AM.png)

If there is not enough RAM memory to map, the program will map some of the program's address space to the disk, when we need it, we bring it into memory.![Screen Shot 2021-01-05 at 5.17.43 AM](/Users/liukun/Documents/Screen/Screen Shot 2021-01-05 at 5.17.43 AM.png)

![Screen Shot 2021-01-05 at 5.19.22 AM](/Users/liukun/Documents/Screen/Screen Shot 2021-01-05 at 5.19.22 AM.png)
# RISC-V Talent Development Program
RISC-V Talent Development Program , powered by samsung Semiconductor India Research(SSIR) along with VLSI System Design(VSD)
# Basic Details 
Name : Sharanya P A <br />
College: Sahyadri College of Engineering and Management, Mangalore <br />
Email ID : sharanya.ec22@sahyadri.edu.in <br />
Github Profile : https://github.com/Sharanya-Sahyadri-ECE <br />
LinkedIN Profile : https://in.linkedin.com/in/sharanya-p-a-259412258  
<br />
# Task 1
## To install the Essential Tools and Set Up Virtual Machine in VirtualBox:
Install VirtualBox-7.1.4-165100-Win.exe and riscv_workshop.vdi. After installation open VirtualBox and click "New" to create a new virtual machine. Select Linux as the operating system with Ubuntu 18.04 (64 bytes) as a version. Allocate memory and Use an existing virtual hard disk file.Browse to the unzipped VDI file where it is located and select it.
### Launch the Virtual Machine :
Once the virtual machine is created, select it and click "start" to boot up the VDI file with the operating system and software.
![Screenshot 2025-01-06 091422](https://github.com/user-attachments/assets/8ce5fabf-94dc-4526-afa5-b25b9b9bec0f)
## Writing, Compiling, and Running a Parameterized C Program Locally
Description: In this task, a C program (sum1ton.c) is written to compute the sum of numbers from 1 to a user-specified value n. The program uses a loop for the computation and dynamically accepts the input from the user during execution. It is compiled using the standard GCC compiler on the local Ubuntu system. After successful compilation, the program displays the sum based on the input value of n. This task highlights the development and execution process for parameterized C programs on a host system.

Steps:
Use a text editor (e.g., leafpad) to write a C program that calculates the sum from 1 to n with user input.
Compile the program using the GCC compiler.

Execute the compiled binary (./a.out) and enter a value for n to compute and display the sum.

The sample program is given by sum1ton.c

![screenshot](https://github.com/user-attachments/assets/0228d67e-0d82-4530-8159-c5cb614cf1a7)

The task involves creating a simple C program (sum1ton.c) that computes the sum of numbers from 1 to 100.

## Compiling and Optimizing a Parameterized C Program for RISC-V Architecture
 In this task, a C program (sum1ton.c) is written to calculate the sum of numbers from 1 to a user-defined value n. The program uses a loop to compute the sum and prompts the user to input the value of n. It is then compiled using a RISC-V cross-compiler (riscv64-unknown-elf-gcc) with optimization flags (-O1 and -Ofast) and specific parameters to define the ABI (-mabi=lp64) and the architecture (-march=rv64i). This ensures that the compiled code is optimized for execution in a 64-bit RISC-V environment. The output is an object file (sum1ton.o), which can be executed in a RISC-V-based simulation or hardware platform. This task demonstrates how to target specific hardware architectures with cross-compilation.

Steps:

Write the sum1ton.c program that calculates the sum from 1 to n.

Could you compile the program using the RISC-V GCC compiler with the appropriate flags for optimization and architecture

Verify the creation of the object file (sum1ton.o) by listing its details.
![Screenshot 2025-01-06 065536](https://github.com/user-attachments/assets/e55d037d-c56d-4757-898d-f03057440132)

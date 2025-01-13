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
To install the essential tools and set up a virtual machine in VirtualBox, first, install VirtualBox-7.1.4-165100-Win.exe and riscv_workshop.vdi. After installation, open VirtualBox and click "New" to create a virtual machine. Select Linux as the operating system and choose Ubuntu 18.04 (64-bit) as the version. Allocate the required memory, then select "Use an existing virtual hard disk file". Browse to the location of the unzipped VDI file, select it, and proceed with the setup.
### Launch the Virtual Machine :
Once the virtual machine is created, select it and click "start" to boot up the VDI file with the operating system and software.
![Screenshot 2025-01-06 091422](https://github.com/user-attachments/assets/8ce5fabf-94dc-4526-afa5-b25b9b9bec0f)
## Writing, Compiling, and Running a Parameterized C Program Locally
In this task, a C program (sum1ton.c) is created to calculate the sum of numbers from 1 to a user-specified value n. The program utilizes a loop for computation and dynamically accepts input from the user during execution. It is compiled using the standard GCC compiler on a local Ubuntu system. Upon successful compilation, the program prompts the user for n, computes the sum, and displays the result. This task demonstrates the development and execution of parameterized C programs on a host system.
Steps:
1. Use a text editor (e.g., leafpad) to write a C program that computes the sum from 1 to n based on user input.
2. Compile the program using the GCC compiler.
3. Run the compiled binary (./a.out), enter a value for n, and view the computed sum.
The sample program is provided in sum1ton.c.

![screenshot](https://github.com/user-attachments/assets/0228d67e-0d82-4530-8159-c5cb614cf1a7)

The task involves creating a simple C program (sum1ton.c) that computes the sum of numbers from 1 to 100.

## Compiling and Optimizing a Parameterized C Program for RISC-V Architecture
In this task, a C program (sum1ton.c) is developed to compute the sum of numbers from 1 to a user-defined value n. The program employs a loop for calculation and prompts the user to enter n. It is then compiled using a RISC-V cross-compiler (riscv64-unknown-elf-gcc) with optimization flags (-O1 and -Ofast) and specific parameters to define the ABI (-mabi=lp64) and architecture (-march=rv64i). This ensures that the generated code is optimized for execution in a 64-bit RISC-V environment. The output is an object file (sum1ton.o), which can be executed on a RISC-V-based simulation or hardware platform. This task demonstrates the process of cross-compiling programs for specific hardware architectures.
Steps:
1. Write the sum1ton.c program to compute the sum from 1 to n.
2. Compile the program using the RISC-V GCC compiler with appropriate flags for optimization and architecture.
3. Verify the creation of the object file (sum1ton.o) by listing its details.
![Screenshot 2025-01-06 065536](https://github.com/user-attachments/assets/e55d037d-c56d-4757-898d-f03057440132)
![401242886-d50cbce4-e138-4033-8d77-8fb5271b125c](https://github.com/user-attachments/assets/f994fca2-f760-4eae-a46b-b09de0c67caf)



# Task 2

## SPIKE SIMULATION 
This task implements a C program in RISC-V cross-compiler(riscv64-unkonown-elf-gcc) with optimization flags -O1 and -Ofast. This ensures the generated code is optimized for execution in a 64-bit RISC-V environment. The output is an object file, which can be executed on a RISC-V-based simulation or hardware platform. This task demonstrates the process of cross-compiling programs for specific hardware architectures.
Steps:
1. Write a Simple C program.
2. Compile the C program using RISC-V GCC/SPIKE with the optimization
3. Generate and collect the RISC-V object dump for both -O1 and -Ofast.
4. observe the different optimizations

The following shows the screenshots of optimizations

![WhatsApp Image 2025-01-13 at 7 16 32 PM (1)](https://github.com/user-attachments/assets/93fa69f3-2350-4b97-9eef-06af1ed4b0bf)

![WhatsApp Image 2025-01-13 at 7 16 31 PM (1)](https://github.com/user-attachments/assets/666b4c13-7ef4-48b1-8c59-3301a5afb20c)

![WhatsApp Image 2025-01-13 at 7 16 32 PM](https://github.com/user-attachments/assets/41edcfe3-77b7-4eaf-a64c-83518676c355)

![WhatsApp Image 2025-01-13 at 7 16 32 PM (1)](https://github.com/user-attachments/assets/fe8be9e1-f8d6-49ff-b6ca-017e354dacd9)

![WhatsApp Image 2025-01-13 at 7 16 32 PM (2)](https://github.com/user-attachments/assets/d3ebe6b0-926f-490a-bd7a-4332a7fb9153)

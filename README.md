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


# Task 3
## Step 1: Review RISC-V Documentation
Open the RISC-V software documentation (provided link) and read about the instruction types:
R-type: Register-Register operations<br>
I-type: Immediate operations & Load instructionss<br>
S-type: Store instructionss<br>
B-type: Branch instructionss<br>
U-type: Upper immediate instructionss<br>
J-type: Jump instructionss<br>
## Step 2: Explore the Sample GitHub Repository
Open the Sample Repo and examine the visual representation of instruction decoding.

Understand how instructions are broken down into opcode, funct3, funct7, register fields, and immediate values.
## Step 3: Obtain riscv-objdump of Your Application Code
Compile your RISC-V application code into an executable using a GCC toolchain:

riscv64-unknown-elf-gcc -o my_program my_program.c
Generate the disassembly output using riscv-objdump:

riscv64-unknown-elf-objdump -d my_program > disassembly.txt

Open disassembly.txt and extract 15 unique instructions.

## Step 4: Identify the Instruction Type for Each Instruction
Determine each extracted instruction's type (R, I, S, B, U, or J).
You can use the instruction format reference from Step 1.
## Step 5: Convert Instructions to 32-bit Binary Patterns
For each instruction:

Identify the opcode, funct3, funct7, source/destination registers, and immediate values.
Construct the binary format based on the instruction type.
Convert the binary format into a 32-bit hexadecimal representation.
Example:
Instruction: add x5, x6, x7 (R-type)

Opcode: 0110011
Funct3: 000
Funct7: 0000000
Registers: rd = 5, rs1 = 6, rs2 = 7
32-bit encoding:


funct7   rs2   rs1   funct3  rd    opcode  
0000000  00111 00110 000     00101 0110011  

Converted to Hex: 0x00628333
## Step 6: Upload to Your GitHub Repository
Create a text file (riscv_32bit_instructions.txt) containing the binary and hex representations of the 15 instructions.
Use Git commands to upload:
 ![402938188-e82da314-af58-47fb-b68a-eb1a51822319](https://github.com/user-attachments/assets/2c240245-bbec-4256-a0d3-1d325d3bd256)

 # Task 4
 Steps to perform functional simulation of RISCV
Download Files: Download the code from the reference github repo.

Set Up Simulation Environment: Install iverlog using commands:

 sudo apt install iverilog
 sudo apt install gtkwave
To run and simulate the verilog code, enter the following command:

 iverilog -o iiitb_rv32i iiitb_rv32i.v iiitb_rv32i_tb.v
 ./iiitb_rv32i
To see the simulation waveform in GTKWave, enter the following command:

 gtkwave iiitb_rv32i.vcd
32-bits instruction used in the code:
![instructions](https://github.com/user-attachments/assets/e04ce9e5-9e4b-41b2-aabf-4a201e2bd05d)


Instructions

Analysing the Output Waveform of various instructions that we have covered in this task.
![add](https://github.com/user-attachments/assets/a8c7e91b-32c1-4fae-b317-15d2f32db6b1)

ADD R6,R1,R2
ADD R6,R1,R2

32 bit instruction:32'h02208300
![sub1](https://github.com/user-attachments/assets/78a25b86-6cb2-464d-8f3a-82358e88a8db)

SUB R7,R1,R2
SUB R7,R1,R2

32 bit instruction:32'h02209380
![and](https://github.com/user-attachments/assets/f523d7ac-34f2-4078-8932-e4a5e4917a27)

And R8,R1,R3
And R8,R1,R3

32 bit instruction:32'h0230a400


OR R9,R2,R5
OR R9,R2,R5

32 bit instruction:32'h02513480

XOR R10,R1,R4
XOR R10,R1,R4

32 bit instruction:32'h0240c500

SLT R11,R2,R4
SLT R11,R2,R4

32 bit instruction:32'h02415580

ADDI R12,R4,5
ADDI R12,R4,5

32 bit instruction:32'h00520600
![beq](https://github.com/user-attachments/assets/908a7b85-90d6-4bca-847a-acc15f16f386)
BEQ R0,R0,15
BEQ R0,R0,15

32 bit instruction:32'h00f00002

git clone <your-repo-link>  <br>
cd <your-repo>
echo "Instruction - 32-bit Binary - Hex" > riscv_32bit_instructions.txt
git add riscv_32bit_instructions.txt
git commit -m "Added 32-bit RISC-V instruction encoding"
git push origin main
**# Steps to Perform Functional Simulation of RISC-V**

## 1. Download Files
Download the code from the reference GitHub repository using:
```sh
git clone <your-repo-link>
cd <your-repo>
```

## 2. Set Up Simulation Environment
Ensure your system has the required tools installed:
```sh
sudo apt update
sudo apt install iverilog gtkwave
```

## 3. Compile and Simulate the Verilog Code
Run the following commands to compile and execute:
```sh
iverilog -o iiitb_rv32i iiitb_rv32i.v iiitb_rv32i_tb.v
./iiitb_rv32i
```

## 4. View Simulation Waveform in GTKWave
```sh
gtkwave iiitb_rv32i.vcd
```

## 5. 32-bit Instructions Used in the Code
Below are the instructions and their corresponding 32-bit representations:

### Arithmetic Operations
- **ADD**  
  **Instruction:** `ADD R6, R1, R2`  
  **Binary:** `32'h02208300`

- **SUB**  
  **Instruction:** `SUB R7, R1, R2`  
  **Binary:** `32'h02209380`

### Logical Operations
- **AND**  
  **Instruction:** `AND R8, R1, R3`  
  **Binary:** `32'h0230a400`

- **OR**  
  **Instruction:** `OR R9, R2, R5`  
  **Binary:** `32'h02513480`

- **XOR**  
  **Instruction:** `XOR R10, R1, R4`  
  **Binary:** `32'h0240c500`

### Comparison Operations
- **SLT (Set Less Than)**  
  **Instruction:** `SLT R11, R2, R4`  
  **Binary:** `32'h02415580`

### Immediate Operations
- **ADDI (Add Immediate)**  
  **Instruction:** `ADDI R12, R4, 5`  
  **Binary:** `32'h00520600`

### Branching Operations
- **BEQ (Branch If Equal)**  
  **Instruction:** `BEQ R0, R0, 15`  
  **Binary:** `32'h00f00002`

## 6. Commit and Push to GitHub Repository
```sh
echo "Instruction - 32-bit Binary - Hex" > riscv_32bit_instructions.txt
git add riscv_32bit_instructions.txt
git commit -m "Added 32-bit RISC-V instruction encoding"
git push origin main
```



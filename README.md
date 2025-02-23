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
**# Steps to Perform Functional Simulation of RISC-V**

## Step 1: Review RISC-V Documentation
Open the RISC-V software documentation (provided link) and review the different instruction types:

- **R-type:** Register-Register operations
- **I-type:** Immediate operations & Load instructions
- **S-type:** Store instructions
- **B-type:** Branch instructions
- **U-type:** Upper immediate instructions
- **J-type:** Jump instructions

Understanding these instruction types will help in analyzing and debugging the application code.

## Step 2: Explore the Sample GitHub Repository
Visit the Sample Repository and examine the visual representation of instruction decoding. This will help in understanding:

- How instructions are broken down into their components: **opcode, funct3, funct7, register fields, and immediate values**.
- The role of different instruction formats in executing various operations within the RISC-V architecture.

## Step 3: Obtain riscv-objdump of Your Application Code
To analyze your RISC-V application, compile it using the GCC toolchain:
```sh
riscv64-unknown-elf-gcc -o my_program my_program.c
```
This will generate an executable `my_program`.

### Generate the Disassembly Output
To view the disassembled instructions:
```sh
riscv64-unknown-elf-objdump -d my_program > disassembly.txt
```

### Extract and Analyze Instructions
- Open `disassembly.txt`
- Identify and extract **15 unique instructions**
- Categorize them into their respective instruction types (**R, I, S, B, U, J**)
- Compare the binary representations with the documented encoding schemes

## Step 4: Functional Simulation Setup
### Download Files
Download the code from the reference GitHub repository using:
```sh
git clone <your-repo-link>
cd <your-repo>
```

### Install Required Tools
Ensure your system has the necessary tools installed:
```sh
sudo apt update
sudo apt install iverilog gtkwave
```

### Compile and Simulate Verilog Code
```sh
iverilog -o iiitb_rv32i iiitb_rv32i.v iiitb_rv32i_tb.v
./iiitb_rv32i
```

### View Simulation Waveform in GTKWave
```sh
gtkwave iiitb_rv32i.vcd
```

## Step 5: 32-bit Instructions Used in the Code
Below are some instructions and their corresponding 32-bit representations:

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

## Step 6: Commit and Push to GitHub Repository
```sh
echo "Instruction - 32-bit Binary - Hex" > riscv_32bit_instructions.txt
git add riscv_32bit_instructions.txt
git commit -m "Added 32-bit RISC-V instruction encoding"
git push origin main
```
 ![402938188-e82da314-af58-47fb-b68a-eb1a51822319](https://github.com/user-attachments/assets/2c240245-bbec-4256-a0d3-1d325d3bd256)

 # Task 4
 
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
![instructions](https://github.com/user-attachments/assets/e04ce9e5-9e4b-41b2-aabf-4a201e2bd05d)

Analysing the Output Waveform of various instructions that we have covered in this task.
![add](https://github.com/user-attachments/assets/a8c7e91b-32c1-4fae-b317-15d2f32db6b1)

![sub1](https://github.com/user-attachments/assets/78a25b86-6cb2-464d-8f3a-82358e88a8db)

![and](https://github.com/user-attachments/assets/f523d7ac-34f2-4078-8932-e4a5e4917a27)

![beq](https://github.com/user-attachments/assets/908a7b85-90d6-4bca-847a-acc15f16f386)

# Task 5 
# Smart LED Control Using RISC-V

## 📌 Overview
This project controls an LED using a push button and a VSD RISC-V board. When the button is pressed, the LED toggles between ON and OFF states. It’s an easy project to understand GPIO input and output operations in RISC-V.

---

## 🛠 Components Required  
| **Component**         | **Quantity** | **Purpose**                  |
|----------------------|-------------|------------------------------|
| **VSD RISC-V Board** | 1           | Microcontroller              |
| **LED (Any Color)**  | 1           | Visual indication            |
| **Push Button**      | 1           | Switch to toggle LED         |
| **330Ω Resistor**    | 1           | Limits current for LED       |
| **10kΩ Resistor**    | 1           | Pull-down resistor for button |
| **Breadboard & Wires** | -         | Circuit connections          |

---

## 🔌 Circuit Connections  
| **Component**      | **Pin on RISC-V Board** | **Function**         |
|-------------------|----------------------|---------------------|
| **LED (+)**      | PA0 (Digital Output)  | LED Control        |
| **LED (-)**      | GND                    | Ground             |
| **Button One End** | PA1 (Digital Input)  | Button Signal      |
| **Button Other End** | GND                 | Pull-down Resistor |

---

## 🚀 Setup & Installation  

### **1️⃣ Connect the Components**  
- Connect **LED anode (+)** to **PA0** and cathode (-) to **GND**.  
- Connect one end of the **button** to **PA1** and the other end to **GND**.  
- Use a **10kΩ pull-down resistor** between PA1 and GND.  

### **2️⃣ Install RISC-V Toolchain**  
```sh
sudo apt update  
sudo apt install gcc-riscv64-unknown-elf  
```

### **3️⃣ Compile the Code**  
```sh
riscv64-unknown-elf-gcc -o led_toggle src/led_toggle.c  
```

### **4️⃣ Run the Simulation (Optional: GTKWave)**  
```sh
iverilog -o led_sim src/led_toggle.v src/led_toggle_tb.v  
vvp led_sim  
gtkwave led_wave.vcd  
```

---

## 📝 Code Snippet (C for VSD RISC-V Board)  
```c
#include <vsd_gpio.h>
#include <vsd_delay.h>

#define LED_PIN 0
#define BUTTON_PIN 1

void setup() {
    gpio_mode(LED_PIN, OUTPUT);
    gpio_mode(BUTTON_PIN, INPUT);
}

void loop() {
    if (gpio_read(BUTTON_PIN) == HIGH) {
        gpio_toggle(LED_PIN);  // Toggle LED state
        delay(300);  // Debounce delay
    }
}
```

---

## 🔗 GitHub Setup & Push  
```sh
git clone https://github.com/yourusername/RISC-V_LED_Control.git  
cd RISC-V_LED_Control  
mkdir src  
touch src/led_toggle.c  
echo "# RISC-V LED Control" > README.md  
git add .  
git commit -m "Initial Commit - LED Toggle Code"  
git push origin main  
```

---

## 🎯 Features & Benefits  
✅ **Simple project for GPIO practice**  
✅ **Teaches button debounce and state toggling**  
✅ **Can be expanded into LED patterns or PWM brightness control**  

---

## 💡 Future Improvements  
🔹 Add **multiple LEDs** to display patterns.  
🔹 Control LED brightness using **PWM**.  
🔹 Add a **buzzer** for sound-based feedback.  


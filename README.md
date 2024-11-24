# VSDSquadron-Research-Internship-20th October Cohert
The program is based on the RISC-V architecture and uses open-source tools to teach people about VLSI chip design and RISC-V. The instructor for this internship is Kunal Ghosh Sir.
## Lab exercises of RISCV workshop
Instructor: Kunal Ghosh
# Task1: Install RISC-V toolchain using VDI.Upload snapshot of compiled C code and RISC-V Objdmp on your GitHub repo
## Description:
The task included downloading a virtual manager and installing the RIS-V toolchain using VDI Write a C code for the sum to n numbers Compile the above code using gcc compiler Compile the above code using the RISC-V simulator
## Installations:
Oracle Virtual machine
![Screenshot (13)](https://github.com/user-attachments/assets/c299495f-9744-41f2-91b6-8d3512e14daf)

Gedit editor
![1](https://github.com/user-attachments/assets/b9ad2f47-889d-44d9-ace3-c87ff91274cc)

## Steps:
1: Open Gedit and write the C code to find the sum of n numbers
![2](https://github.com/user-attachments/assets/b7dc646a-153b-4e4d-8ef0-0eae38c20426)

2:Compile the above code using gcc and get the output
![3](https://github.com/user-attachments/assets/c088306e-a8d8-42fe-a01b-e980d82bc80c)

3:Now, compile and run the same code using the RISC-V Simulator and search for main using the command: "riscv64-unknown-elf-objdump -d sum.o | less" and then type out "/main"
![5](https://github.com/user-attachments/assets/15d8cd8a-aaf7-45fc-8d60-ef1183de7100)

4:Changing it from O1 to Ofast: 
![6](https://github.com/user-attachments/assets/8ab5d62a-5068-4440-be84-338a86d9d1f9)

5:Search for main usin the commands: "riscv64-unknown-elf-objdump -d sum.o | less" and then type out "/main"
![7](https://github.com/user-attachments/assets/55704bcb-b96e-4392-bb3a-380e46c25fed)

# Task 2:
## A.SPIKE simulation and observation with -O1 and -Ofast.upload snapshots of compiled C code,RISC-V Objdump
## What is SPIKE in RISC-V?
A RISC-V ISA is a simulator, enabling the testing and analysis of RISC-V programs without the need for actual hardware.
Spike is a free, open-source C++ simulator for the RISC-V ISA that models a RISC-V core and cache system. It can be used to run programs and a Linux kernel, and can be a starting point for running software on a RISC-V target
## Steps:
1.The C code is the same as above: 
![2](https://github.com/user-attachments/assets/61aa28ae-234f-4cc4-8fbd-7439060320c4)

2.Ofast: output using risc simulator
![7](https://github.com/user-attachments/assets/36a11653-1c45-4ba9-95ba-aee2b1c485b7)

3.Confirming the same using spike and debugging
![9](https://github.com/user-attachments/assets/2be6b798-614b-433d-bd66-e9217f3b40cb)

This method confirms all the three methods give the same output
## B.Write a simple C program for any simple application and RISC-V GCC/SPIKE
## Steps:
1.C code of calculator application
![10](https://github.com/user-attachments/assets/bd46bec1-e3ae-4a9a-9f50-a0aa21818ab7)

![11](https://github.com/user-attachments/assets/ef8f95ad-0c10-451f-b10d-9c4b76800119)

2.Compile it using gcc
![12](https://github.com/user-attachments/assets/e4fcfa17-f8d7-4483-ada1-fff9cfbf742a)

3.Compile it using RISC simulator
![13](https://github.com/user-attachments/assets/4ee802cc-2ee9-4948-826e-3f1377f7d850)

4.Compile it using SPIKE simulator
![14](https://github.com/user-attachments/assets/9699e44d-30e5-42aa-8c73-c7035c803c31)
All three compilers/simulators produce the same output

# TASK 3:-
## RISC-V Instruction Types (R,I,S,B,U,J):
The RISC-V instruction set architecture (ISA) defines several types of instructions, each with a specific format. Below is a summary of the main instruction types:
![382201566-e9b6a795-6e82-4ea6-9feb-129a8dc1bc9b](https://github.com/user-attachments/assets/819cd11f-3ebe-4959-8890-9e546ed7e3cb)

### 1.) R-Type (Register-Register):
Purpose: Used for operations that involve two source registers and one destination register

Fields:

opcode: Operation code

rd: Destination register

func3: Function modifier

rs1: Source register 1

rs2: Source register 2

func7: Function modifier (additional)

Example: add x1, x2, x3

### 2.) I-Type (Immediate):
Purpose: Used for operations with one source register and an immediate value, including loads.

Fields:

opcode: Operation code

rd: Destination register

func3: Function modifier

rs1: Source register

imm[11:0]: Immediate value

Example: addi x1, x2, 10

### 3.) S-Type (Store):
Purpose: Used for store instructions, which write a register's value to memory.

Fields:

opcode: Operation code

imm[11:5]: Immediate value (upper 7 bits)

func3: Function modifier

rs1: Source register (base address)

rs2: Source register (data to store)

imm[4:0]: Immediate value (lower 5 bits)

Example: sw x2, 0(x1)

### 4.) B-Type (Branch):
Purpose: Used for conditional branch instructions.

Fields:

opcode: Operation code

imm[12]: Immediate value (bit 12)

imm[10:5]: Immediate value (bits 10 to 5)

func3: Function modifier

rs1: Source register 1

rs2: Source register 2

imm[4:1]: Immediate value (bits 4 to 1)

imm[11]: Immediate value (bit 11)

Example: beq x1, x2, label

### 5.) U-Type (Upper Immediate):
Purpose: Used for instructions that operate with a large immediate value.

Fields:

opcode: Operation code

rd: Destination register

imm[31:12]: Immediate value

Example: lui x1, 0x10000

### 6.) J-Type (Jump):
Purpose: Used for jump instructions with a large immediate value.

Fields:

opcode: Operation code

rd: Destination register

imm[20]: Immediate value (bit 20)

imm[10:1]: Immediate value (bits 10 to 1)

imm[11]: Immediate value (bit 11)

imm[19:12]: Immediate value (bits 19 to 12)

Example: jal x1, label

# 32-bit Instruction Codes in RISC-V Instruction Type Format for 15 Unique Instructions:
### 1.) addi x1, x2, 10

Instruction Format: I-type

Binary Encoding: 000000000010 00010 000 00001 0010011

32-bit Instruction Code: 0x00210093

### 2.) li x5, 0x0

Instruction Format: I-type (using addi x5, x0, 0x0)

Binary Encoding: 000000000000 00000 000 00101 0010011 

32-bit Instruction Code: 0x00000293

### 3.) lui x10, 0x20000

Instruction Format: U-type

Binary Encoding: 00100000000000000000 01010 0110111

32-bit Instruction Code: 0x20000537

### 4.) mv x1, x2

Instruction Format: I-type (using addi x1, x2, 0)

Binary Encoding: 000000000000 00010 000 00001 0010011

32-bit Instruction Code: 0x00010093

### 5.) sw x5, 0(x10)

Instruction Format: S-type

Binary Encoding: 0000000 00101 01010 010 00000 0100011

32-bit Instruction Code: 0x0050a023

### 6.) lw x5, 0(x10)

Instruction Format: I-type

Binary Encoding: 000000000000 01010 010 00101 0000011

32-bit Instruction Code: 0x0000a283

### 7.)jal x0, 0x100

Instruction Format: J-type

Binary Encoding: 00000000000100000000 00000 1101111

32-bit Instruction Code: 0x0000086f

### 8.) beq x1, x2, label

Instruction Format: B-type (assuming offset is 0x4)

Binary Encoding: 000000 00010 00001 000 00010 1100011

32-bit Instruction Code: 0x00210063

### 9.) bne x1, x3, label

Instruction Format: B-type (assuming offset is 0x4)

Binary Encoding: 000000 00011 00001 001 00010 1100011

32-bit Instruction Code: 0x00310063

### 10.) slli x5, x1, 1

Instruction Format: I-type

Binary Encoding: 0000000 00001 00101 001 00001 0010011

32-bit Instruction Code: 0x00109093

### 11.) srli x6, x2, 2

Instruction Format: I-type

Binary Encoding: 0000000 00010 00110 101 00010 0010011

32-bit Instruction Code: 0x0022b093

### 12.) and x3, x4, x5

Instruction Format: R-type

Binary Encoding: 0000000 00101 00100 111 00011 0110011

32-bit Instruction Code: 0x005201b3

### 13.) or x2, x3, x4

Instruction Format: R-type

Binary Encoding: 0000000 00100 00011 110 00010 0110011

32-bit Instruction Code: 0x004181b3

### 14.) sub x3, x5, x2

Instruction Format: R-type

Binary Encoding: 0100000 00010 00101 000 00011 0110011

32-bit Instruction Code: 0x402282b3

### 15.) xor x1, x2, x3

Instruction Format: R-type

Binary Encoding: 0000000 00011 00010 100 00001 0110011

32-bit Instruction Code: 0x003100b3

# Task 4:
## By making use of RISC-V Core: Verilog Netlist and Testbench, perform an experiment of Functional Simulation and observe the waveforms
NOTE: Since the designing of RISCV Architecture and writing it's testbench is not the part of this Research Internship, so we will use the Verilog Code and Testbench of RISCV that has already been designed. The reference GitHub repository is : iiitb_rv32i

## Steps to perform functional simulation of RISCV
GTKWAVE Generation Process
Follow the steps below to generate the waveform using Verilog code and GTKWAVE.

### Step 1: Clone the Repository
Clone the RISC-V Verilog repository using the git clone command.

git clone https://github.com/vinayrayapati/rv321
### Step 2: Navigate to the Cloned Directory
Change the directory to the cloned repository.

cd rv321
### Step 3: Compile the Verilog Code and Testbench
Run the following iverilog command to compile the Verilog code and testbench.

iverilog -o iiitb_rv32i iiitb_rv32i.v iiitb_rv32i_tb.v
### Step 4: Simulate the Verilog Code
After compiling, simulate the Verilog code by running the compiled file:

./iiitb_rv321
![15](https://github.com/user-attachments/assets/0bcf9bd9-d934-49d6-9e8b-2093bdcc581c)


### Step 5: Open the Waveform in GTKWAVE
Once the simulation generates the .vcd (Value Change Dump) file, you can visualize the waveform in GTKWAVE.

gtkwave iiitb_rv321.vcd
It will open the new window of GTKWAVE

![gtkwave 1](https://github.com/user-attachments/assets/f4f16095-9277-4fc4-9590-8fee9c7133fb)

Tap the iiitb_rv32i_tb in the SST section

![gtkwave 2](https://github.com/user-attachments/assets/5c0260f4-560a-4ce4-bcd3-882f70881986)

Now, drag the command in the same way presented under time section.

![gtkwave 4](https://github.com/user-attachments/assets/4a3c0a80-1e8e-4278-a301-0184db58dfdc)

Select the instructions from EX_MEM_IR[31:0] to present the instructions used in Task 3 and Analysing the Output Waveform of various instructions that we have covered in TASK-3.

#### Instruction ADD r1, r2, r3 :
![ADD r1,r2,r3](https://github.com/user-attachments/assets/b353af89-7f46-4156-a106-51fe62643b0b)

#### Instruction SUB r3, r1, r2 :
![SUB r3, r1, r2](https://github.com/user-attachments/assets/baef2e50-a17e-4f1c-a9d9-252daf8a880e)

#### Instruction AND r2, r1, r3 :
![AND r2, r1, r3](https://github.com/user-attachments/assets/e999ab06-c4a5-4d58-ae4e-55cecd94094f)

#### Instruction OR r8, r2, r5 :
![OR r8, r2, r5](https://github.com/user-attachments/assets/571f5828-2e9a-40ad-b987-576bebb946e9)

#### Instruction XOR r8, r1, r4 :
![XOR r8, r1, r4](https://github.com/user-attachments/assets/7e25aded-599b-4563-90fe-c57c4c9955da)

#### Instruction SLL r15, r11, r2 :
![SLL r15, r11, r2](https://github.com/user-attachments/assets/43d56b5d-4a3f-40da-a87d-620f67e9a3ad)

#### Instruction SLT r10, r2, r4 :
![SLT r10, r2, r4](https://github.com/user-attachments/assets/e56c855a-7a6d-4673-9e7b-7213047743f5)

To conclude : The output waveform for the list of instructions are obtained in GTKWAVE.

# Task 5
## Implementation of Bluetooth automated smart access
### Introduction
Technology's seamless integration into our lives has turned smart homes from a vision into reality. Central to this is the “Bluetooth Automated Smart Access” system, combining convenience, security, and innovation. Using a VSD Squadron Mini board, Bluetooth module, and servo motor, this system simplifies interactions with our living spaces.

Unlike traditional manual methods that are cumbersome, this technology allows users to control devices via smartphone, reducing physical interaction. Applications include managing water taps, lighting, appliances, smart doors, and security systems, making daily tasks more efficient and streamlined.

### Overview:
This project introduces an innovative door access control system using a servo motor, Bluetooth module, push-button, and onboard LED. The system operates by triggering the servo motor to open or close upon receiving a Bluetooth command. The VSD Squadron Mini activates the motor, enabling a hands-free, user-friendly, and secure access mechanism.

Key Components:

- Servo Motor (Pin PC6): Functions as the lock, controlled by the microcontroller.
- Bluetooth Module (Pins PD6, PD7, PC7, GND, 3.3V): Facilitates wireless communication for remote control; the State pin shows connection status.
- Onboard LED (LED_BUILTIN): Indicates locked/unlocked status for visual feedback.
Users can control the system via smartphone, with the LED enhancing user experience and reliability. This project highlights a practical IoT solution for home security and automation.

### Components Required with description:

- VSD Squadron Mini – 1 (Microcontroller board)
- Servo Motor (e.g., SG90) – 1 (Standard servo motor)
- Bluetooth HC-05 Module – 1 (Bluetooth module for serial communication)
- Jumper Wires – 1 set (Male-to-male and female-to-male jumper wires)
- Micro USB Cable – 1 (For programming and power supply)

### Pin connections:
![Screenshot (35)](https://github.com/user-attachments/assets/cbdf1986-9744-40b7-bd71-54a015bb756e)

### Pinout diagram:
![Screenshot (34)](https://github.com/user-attachments/assets/1c612304-84f4-41b4-8681-de451e95a52d)

# Task 6:
## Upload Final working code and short video of the application

### Code snippet:
![Screenshot (37)](https://github.com/user-attachments/assets/1f7f027d-70a3-4389-a62b-02af6b979641)

![Screenshot (38)](https://github.com/user-attachments/assets/f47a1036-5c1b-4532-aca0-21a474876b6c)

![Screenshot (39)](https://github.com/user-attachments/assets/bd443d72-20d5-44ac-b690-0626f9c01bda)

![Screenshot (40)](https://github.com/user-attachments/assets/b89da470-c2b2-4e13-b88f-e98a2c710fbb)
### Video of application




### Acknowledgement 

I would like to express my gratitude to Kunal Ghosh Sir for giving me the opportunity to delve into the RISCV Architecture through this internship with VSDSquadron Mini. This experience has not only been an inspiring introduction to the field but has also sparked my curiosity and significantly enhanced my technical skills. I would also like to extend my heartfelt thanks to VLSI System Design for providing such a meaningful and enriching learning experience that has greatly contributed to my personal and professional development.


















# VSDSquadron-Research-Internship-2024
The program is based on the RISC-V architecture and uses open-source tools to teach people about VLSI chip design and RISC-V. The instructor for this internship is Kunal Ghosh Sir.
# Lab exercises of RISCV workshop
Instructor: Kunal Ghosh
# Task1: Install RISC-V toolchain using VDI.Upload snapshot of compiled C code and RISC-V Objdmp on your GitHub repo
# Description:
The task included downloading a virtual manager and installing the RIS-V toolchain using VDI Write a C code for the sum to n numbers Compile the above code using gcc compiler Compile the above code using the RISC-V simulator
# Installations:
Oracle Virtual machine
![Screenshot (13)](https://github.com/user-attachments/assets/c299495f-9744-41f2-91b6-8d3512e14daf)

Gedit editor
![1](https://github.com/user-attachments/assets/b9ad2f47-889d-44d9-ace3-c87ff91274cc)

# Steps:
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

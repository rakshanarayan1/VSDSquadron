# VSDSquadron-Research-Internship-20th October Cohert
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

# Task 2:
# A.SPIKE simulation and observation with -O1 and -Ofast.upload snapshots of compiled C code,RISC-V Objdump
# Steps:
1.The C code is the same as above: 
![2](https://github.com/user-attachments/assets/61aa28ae-234f-4cc4-8fbd-7439060320c4)

2.Ofast: output using risc simulator
![7](https://github.com/user-attachments/assets/36a11653-1c45-4ba9-95ba-aee2b1c485b7)

3.Confirming the same using spike and debugging
![9](https://github.com/user-attachments/assets/2be6b798-614b-433d-bd66-e9217f3b40cb)

This method confirms all the three methods give the same output
# B.Write a simple C program for any simple application and RISC-V GCC/SPIKE
# Steps:
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







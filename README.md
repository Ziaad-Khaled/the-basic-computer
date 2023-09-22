# Project Description

## Overview

Welcome to the project! In this assignment, I have implemented a combinational control circuit for a specific program. This project focuses on analyzing and adding control gates for registers, memory, and the E unit for a given program.
The project is implemented using **LogiSim**, a digital circuit simulator.

## Specific Tasks

1. **Analyze and Add Control Circuits**: The primary objective is to enhance the provided implementation by adding control circuits that enable the execution of the instructions found in the provided program.

2. **Program Instructions**: The focus is on implementing the instructions specified in the program below. The program's objective is to perform a subtraction of two double-precision numbers, resulting in Z = X - Y.

   ```assembly
   ORG 100
   LDA YL / Load the lower part of Y into AC
   CMA
   INC / Calculate the 2's complement
   ADD XL
   STA ZL / Store the subtracted value of the lower part in ZL
   CLA
   CIL
   STA TMP / Save any overflow that occurred in E to a temporary register
   LDA YH / Load the higher part of Y into AC
   CMA / Complement without increment (increment was done in YL)
   ADD XH
   ADD TMP / Add the overflow saved in TMP to the higher part
   STA ZH / Store the subtracted value of the higher part in ZH
   HLT
   XL, DEC 2505
   XH, DEC 1560
   YL, DEC 480 / YL is initialized to avoid increments where Cout is not in E
   YH, DEC 40
   ZL, DEC 0
   ZH, DEC 0
   TMP, DEC 0
   END
   ```
![image](https://github.com/Ziaad-Khaled/the-basic-computer/assets/77291238/c4d6d392-3b26-4720-bb43-41d1372619e7)

## Getting Started

To begin working on this project:

1. Clone the repository to your local machine.

2. Install LogiSim if you haven't already.

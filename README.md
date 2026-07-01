# CMOS 1-Bit Arithmetic Logic Unit (ALU) Using Transistor-Level CMOS Design

A transistor-level implementation of a **1-bit Arithmetic Logic Unit (ALU)** designed and simulated in **NI Multisim 14.2** using **Static CMOS Logic**. The ALU performs sixteen logical and arithmetic operations selected using a **16:1 Multiplexer**.

---

# Project Overview

The objective of this project is to design and simulate a **1-bit CMOS ALU** entirely at the transistor level using CMOS technology. Every functional block was individually designed, verified, and then integrated into the final ALU.

Unlike HDL-based implementations, this project demonstrates how digital logic is physically realized using complementary **PMOS** and **NMOS** transistor networks.

---

# CMOS Logic

CMOS (Complementary Metal Oxide Semiconductor) is the dominant technology used for modern digital integrated circuits due to its low static power consumption, high noise immunity, and high integration density.

A CMOS logic gate consists of two complementary transistor networks:

- **Pull-Up Network (PUN)** implemented using PMOS transistors.
- **Pull-Down Network (PDN)** implemented using NMOS transistors.

During steady-state operation, only one of these networks conducts, resulting in very low static power dissipation.

---

# PMOS and NMOS

### PMOS
- Turns ON when the gate receives Logic '0'
- Forms the Pull-Up Network
- Efficiently passes Logic HIGH

### NMOS
- Turns ON when the gate receives Logic '1'
- Forms the Pull-Down Network
- Efficiently passes Logic LOW

The complementary operation of PMOS and NMOS enables CMOS circuits to achieve full voltage swing with low power consumption.

---

# Transmission Gate

A Transmission Gate is implemented using **one PMOS transistor and one NMOS transistor connected in parallel**.

The NMOS gate is driven by the control signal, while the PMOS gate is driven by its complement.

This complementary arrangement allows the transmission gate to pass both Logic HIGH and Logic LOW efficiently without the threshold voltage loss associated with a single MOS transistor.

In this project, transmission gates are used to implement:

- PASS A
- PASS B

---

# ALU Operations

| Select (DCBA) | Operation |
|--------------:|-----------|
|0000|NOT A|
|0001|NOT B|
|0010|OR|
|0011|AND|
|0100|NAND|
|0101|NOR|
|0110|XOR|
|0111|XNOR|
|1000|SUM|
|1001|CARRY|
|1010|DIFFERENCE|
|1011|BORROW|
|1100|INCREMENT A|
|1101|INCREMENT B|
|1110|PASS A|
|1111|PASS B|

---

# Working Principle

The ALU accepts two one-bit inputs, **A** and **B**, which are simultaneously applied to all logic and arithmetic blocks.

Each circuit independently computes its corresponding output, such as AND, OR, XOR, SUM, DIFFERENCE, PASS A, and PASS B.

The outputs of all sixteen functional blocks are connected to the inputs of a **16:1 Multiplexer**.

Four select lines (**D, C, B, and A**) determine which operation is forwarded to the final output.

Whenever the select inputs change, the multiplexer routes the selected operation to the output without affecting the remaining functional blocks.

This modular approach allows multiple arithmetic and logical operations to be implemented in a single ALU while using only one output terminal.

---

 

# Applications

- Arithmetic Logic Units (ALUs)
- Processor Datapaths
- Digital Integrated Circuits
- CMOS Logic Design
- Embedded Systems
- VLSI Education

---

# Future Improvements

- 4-bit CMOS ALU
- Carry Propagation Logic
- Status Flag Generation
- Cadence Virtuoso Layout
- Verilog RTL Implementation
- FPGA Implementation

---

# Learning Outcomes

This project provided practical experience in:

- Static CMOS Logic Design
- PMOS/NMOS Transistor-Level Design
- CMOS Gate Implementation
- Transmission Gate Design
- Multiplexer-Based Data Selection
- Arithmetic Circuit Design
- Digital Circuit Simulation
- Modular CMOS System Design

---

# Author
**Pothuganti Divya Sree**

B.Tech – Electronics and Communication Engineering

National Institute of Technology Rourkela

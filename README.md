# ⚙️ Structural Design of a 2-Digit BCD Adder (Ripple Carry vs Look-Ahead)


## 🧾 Summary

This project showcases the complete structural implementation and verification of a **2-digit Binary Coded Decimal (BCD) Adder (8-bit)** using **Verilog-HDL**, completed in two phases:

- **Stage 1**: Ripple Carry Adder (RCA).
- **Stage 2**: Carry Look-Ahead Adder (CLA).


## 🔍 Project Breakdown

### 🔢 Stage 1 – Ripple Carry BCD Adder
- Built using chained **1-bit Full Adders** using basic gates (AND, OR, XOR, etc.).
- Extended to 4-bit adder, then to 1-digit BCD, then 2-digit BCD.
- Verified against all input combinations using a custom testbench.
- Errors logged with time and failure location.
- Worst-case delay calculated → used to derive max clock frequency.

### 🚀 Stage 2 – Carry Look-Ahead BCD Adder
- Designed **4-bit CLA adder** structurally with gate-level components.
- Reduced latency by parallelizing carry computation.
- Constructed full 2-digit BCD adder using two CLA-based digits.
- Reused Stage 1 testbench with modified architecture.
- Adjusted clock cycles to match worst-case delay of CLA-based adder.
- Error detection mechanism validated against mismatches.



## 🧰 Technologies & Tools

- **Language**: Verilog HDL. 
- **Simulation Tool**: ALDEC Active-HDL.
- **Logic Style**: Structural + Behavioral.
- **Gate Delays Used**:
  - XOR: 12 ns.
  - AND/OR: 8 ns.
  - NAND/NOR: 6 ns.
  - Inverter: 3 ns.



## 📊 Key Results

- ✅ Successfully simulated 2-digit BCD adder with error detection.
- 🕒 Measured delay difference between RCA and CLA.  
- ⚡ CLA-based adder showed significant improvement in timing.  
- 🧠 Learned parallel vs serial carry propagation.  
- 🛠️ Developed reusable testbench and analyzer entities.




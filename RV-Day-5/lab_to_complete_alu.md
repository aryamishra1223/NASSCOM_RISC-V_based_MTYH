# 59-RV_D5SK2_L4_Lab_To_Code_Complete_ALU

Overview

This lecture completes the Arithmetic Logic Unit (ALU) implementation for the remaining concerned RV32I instructions.

The lecture focuses on:

- complete ALU functionality for concerned instructions
- arithmetic operations
- logical operations
- comparison operations
- shift operations
- immediate instruction execution
- register-register operations
- ALU result selection

This lecture extends the ALU from supporting only a few instructions (ADD, ADDI) into supporting the complete concerned RV32I instruction set.

---

# Verilog Operator Mapping

Most RV32I instructions directly map onto native Verilog operators:
| Operation   | Verilog Operator |   |
| ----------- | ---------------- | - |
| Add         | `+`              |   |
| Subtract    | `-`              |   |
| AND         | `&`              |   |
| OR          | `Pipe operator`  |   |
| XOR         | `^`              |   |
| Shift Left  | `<<`             |   |
| Shift Right | `>>`             |   |

---

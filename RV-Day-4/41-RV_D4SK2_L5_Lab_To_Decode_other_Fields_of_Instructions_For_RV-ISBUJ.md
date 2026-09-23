
# Relevant Fields

The decoder extracts:
| Field  | Purpose                    |
| ------ | -------------------------- |
| opcode | instruction category       |
| rd     | destination register       |
| rs1    | source register 1          |
| rs2    | source register 2          |
| funct3 | operation subtype          |
| funct7 | extended operation subtype |

---

# RISC-V ISA Property

Each of the fields in the instruction is always coming from the same place regardless of the instruction type. This is an intentional RISC-V design choice. However, Unlike:

- rs1
- rs2
- rd
- funct fields
- opcode

immediate fields vary across instruction formats.

---
 Why Uniform Field Placement Matters

Uniform field positioning greatly simplifies hardware decode logic. The decoder can directly slice bits without instruction-type conditionals. There's no conditioning based on the instruction type.
Meaning - field extraction becomes direct combinational wiring.

---

# Decode Datapath

The decode flow now becomes:
```text
Instruction →
Field Extraction →
Control Logic →
Execution
```
---
<img width="1855" height="954" alt="Image" src="https://github.com/user-attachments/assets/351fe365-75ab-4128-8781-825e7615f167" />

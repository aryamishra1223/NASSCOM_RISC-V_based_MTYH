# 40-RV_D4SK2_L4_Lab_For_Instruction_Immediate_Decode_Logic_For_RV-ISBUJ

## Overview

This lecture implements immediate decode logic for RV-ISBUJ instruction formats. The lecture explains how immediate values are extracted from RISC-V instructions. The lecture focuses on:

- immediate field construction
- instruction-type dependent decoding
- sign extension
- concatenation
- bit replication
- 32-bit immediate generation

Immediate operands are required by:
  - ALU operations
  - loads/stores
  - branches
  - jumps
  - upper immediate instructions

  ---

  # Immediate Fields Depend On Instruction Type

Based on the instruction type, the instruction will have immediate bits in different locations.

---

# RV-ISBUJ Formats

| Type | Meaning         |
| ---- | --------------- |
| I    | Immediate       |
| S    | Store           |
| B    | Branch          |
| U    | Upper Immediate |
| J    | Jump            |

---
## Decode Logic Flow

The immediate decode process becomes:
```text
Instruction →
Instruction Type →
Immediate Bit Selection →
Sign Extension →
32-bit Immediate
```


---

<img width="1855" height="954" alt="Image" src="https://github.com/user-attachments/assets/351fe365-75ab-4128-8781-825e7615f167" />

---

# Hardware Perspective

Immediate values are reconstructed entirely through combinational bit manipulation logic. The CPU does not "compute" immediates mathematically. Instead it:

- rearranges bits
- concatenates fields
- performs sign extension

using combinational wiring logic.

---

# Key Learning Outcome

After this lecture, the learner understands:

- immediate field extraction
- sign extension
- concatenation syntax

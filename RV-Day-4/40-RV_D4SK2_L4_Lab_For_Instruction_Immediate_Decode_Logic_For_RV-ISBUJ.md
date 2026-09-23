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

![Immediate Decode](images/lec40/Immediate_Decode.png)

![Immediate Decode TLV](images/lec40/Immediate_Decode_TLV.png)

[Click Here To Open the Decode implementation in Makerchip](https://makerchip.com/v132/ide/~0ADf9hjY/p-0vghED)

---

<img width="1855" height="954" alt="Image" src="https://github.com/user-attachments/assets/ae7c9d7a-9e0f-4e69-81bf-534127c4a9d4" /> 

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

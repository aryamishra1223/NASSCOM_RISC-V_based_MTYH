# 49-RV_D4SK3_L6_Lab_For_Implementing_Branch_Instructions

## Overview

This lecture begins implementation of branch instruction support for the RISC-V CPU. The lecture focuses on:

- conditional branch instructions
- branch condition evaluation
- signed vs unsigned comparisons
- branch-taken logic

  ---

  At this point:
- the processor pipeline is mostly functional
- but execution stops correctly looping only after branch support is added.

This lecture enables:
- loop execution
- iterative program flow
- conditional control transfer

inside the processor.

---

# Branch vs Jump

An ISA distinction:
| Instruction Type | Behavior      |
| ---------------- | ------------- |
| Branch           | Conditional   |
| Jump             | Unconditional |

---

# Branch Conditions

Branch instructions compare:

- source register 1
- source register 2

and determine whether control flow changes.

---

# Supported Branch Instructions

| Instruction | Meaning                             |
| ----------- | ----------------------------------- |
| BEQ         | Branch if Equal                     |
| BNE         | Branch if Not Equal                 |
| BLT         | Branch if Less Than                 |
| BGE         | Branch if Greater or Equal          |
| BLTU        | Branch if Less Than Unsigned        |
| BGEU        | Branch if Greater or Equal Unsigned |

---

# Signed vs Unsigned Comparisons

Verilog comparisons are unsigned by default. Therefore signed comparisons require special handling.

---

# Branch Taken Signal

```text
taken_branch
```
This signal determines whether branch redirection occurs.

---

# Default Branch Behavior

Non-branch instructions must default to not taken.

---
# Branch Datapath

The datapath now becomes:
```text
Instruction →
Decode →
Register Read →
Comparison →
Branch Decision
```

---

# Loop Execution

Branch support is necessary for loop iteration. Without branches the CPU cannot repeat instructions.

---
<img width="1837" height="965" alt="Image" src="https://github.com/user-attachments/assets/36d7a66f-a8a4-4be7-bff2-17b985a91a32" />
<img width="1838" height="890" alt="Image" src="https://github.com/user-attachments/assets/ca54682b-e634-4f30-a611-42294c10e8c0" />
<img width="1844" height="955" alt="Image" src="https://github.com/user-attachments/assets/78b14b60-c64c-4203-920d-6f0735fad966" />

# 37-RV_D4SK2_L1_Implementation_Plan_and_Lab_for_PC

## Overview

This lecture begins the actual implementation of the RISC-V CPU datapath. This lecture specifically implements Next PC Logic, which controls:

- instruction sequencing
- program execution order
- instruction fetch progression

The lecture introduces:
- PC incrementing
- sequential execution
- byte-addressed PCs
- reset-aware PC initialization
- previous transaction reset handling
- first instruction correctness
- instruction sequencing

This is the first hardware block of the RISC-V processor implementation.

---

# Sequential Execution Assumption

Initially CPU assumes purely sequential execution. Branches will be handled later. This simplifies initial PC implementation.

---

# Goal of First PC Logic

Initial objective is to simply increment PC continuously.

---

# PC Recirculation

The next PC value becomes previous PC plus instruction increment.
Meaning - recirculation path through flip-flops.

---

# Reset MUX Input

During reset mux selects zero, otherwise selects incremented PC.

---



---

# Hardware Perspective

Instruction sequencing is fundamentally state recirculation. The PC continuously feeds back through: 
- flip-flops 
- increment logic
- branch redirection logic

forming the core execution loop of the processor.

---

# Key Learning Outcome

After this lecture, the learner understands:

- next PC logic
- sequential instruction execution
- byte-addressed PCs

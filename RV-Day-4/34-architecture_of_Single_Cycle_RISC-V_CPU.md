## Overview

The lecture introduces:

- CPU microarchitecture
- program counter
- instruction memory
- decode logic
- register file
- ALU
- branch computation
- load/store datapaths
- memory addressing
- writeback
- instruction flow

---

# RISC-V ISA vs Microarchitecture

RISC-V is the instruction set architecture, not the microarchitecture.
| Term              | Meaning                           |
| ----------------- | --------------------------------- |
| ISA               | Defines instructions and behavior |
| Microarchitecture | Hardware implementation of ISA    |

---

# CPU Microarchitecture

## Program Counter (PC)
The PC acts as a pointer into the instruction memory.
Meaning - points to next instruction to execute.

### Instruction Fetch

PC is sent into instruction memory. The instruction memory returns instruction bits.

## Instruction Memory

The PC acts as index into instruction memory. The data that comes back from the instruction memory is the instruction itself.

## Decode Logic

After fetching instruction CPU must interpret it. That's what the decode logic does.

---


# Instruction Memory Timing

Address is sent one cycle and instruction is received next cycle.

---

![RISC-V CPU](images/lec34/RISC-V_CPU.png)

---

<img width="889" height="490" alt="image" src="https://github.com/user-attachments/assets/09ae03c6-b182-410d-a929-86a6fa903536" />

--- 
# Key Hardware Insight

A CPU is fundamentally a datapath plus control. This lecture introduces the datapath structure which later combines with:

- control logic
- pipelining
- hazard handling

to form a complete processor.

---

# Key Learning Outcome

After this lecture, the learner understands:

- RISC-V ISA vs microarchitecture
- CPU datapath structure
- instruction fetch
- decode

# 38-RV_D4SK2_L2_Lab_For_Instruction_Fetch_Logic

## Overview

This lecture implements instruction fetch logic for the RISC-V CPU. The lecture introduces:

- instruction memory hookup
- IMEM interfaces
- instruction fetch
- instruction addressing
- byte-addressed PCs
- aligned instruction access
- memory indexing
- CPU visualization integration
- interface debugging
- produced/consumed signals

This lecture is the first time the CPU actually fetches instructions from instruction memory. The CPU now progresses from instruction sequencing to actual instruction retrieval.

# Instruction Memory Already Provided

The shell already contains instruction memory infrastructure. The instruction memory already contains the summation test program.
Meaning - previously assembled RISC-V program is now stored inside instruction memory.

---

# IMEM Instantiation

We instantiate instruction memory.

---

# IMEM Interface Signals

The instruction memory requires:
| Signal            | Purpose                  |
| ----------------- | ------------------------ |
| IMEM Read Enable  | Enable instruction fetch |
| IMEM Read Address | Instruction address      |
| IMEM Data         | Instruction output       |

## IMEM Read Enable

The CPU must assert read enable to fetch instructions.

## IMEM Read Address

The PC provides instruction address.

### Address Width Consideration

Instruction memory array size determines address width.

---
# Hardware Perspective

Instruction fetch converts control flow into executable data flow. The Program Counter selects memory address which then produces instructions which drive the rest of the processor pipeline.

---

<img width="1851" height="826" alt="Image" src="https://github.com/user-attachments/assets/5fe33885-6b33-4631-9bb3-440254f1cac5" />

---

# Key Learning Outcome

After this lecture, the learner understands:

- instruction fetch logic
- instruction memory interfaces
- IMEM hookup
- aligned instruction addressin

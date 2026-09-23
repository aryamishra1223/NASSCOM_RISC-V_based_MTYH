# 13-RV_D2SK2_L1_Study_New_Algorithm_For_Sum_1_to_N_Using_ASM

## Introduction

This lecture introduces a new approach for calculating:

```text id="jlwm302"
Sum of numbers from 1 to N
```
using ABI registers, function calls and RISC-V assembly language

The lecture demonstrates:

- interaction between C and Assembly
- usage of ABI names
- passing arguments through registers
- returning results through registers
- loop implementation using assembly logic

---

## Original Problem

Compute:
```text
1 + 2 + 3 + ... + N
```
Previously the entire computation was done in C. Now the computation logic is moved into assembly language.

---

## Interaction Between C and Assembly

The lecture explains the complete flow:
```text
Main C Program
      ↓
Function Call
      ↓
Assembly Language Program
      ↓
Perform Computation
      ↓
Return Final Result
      ↓
Back to Main C Program
```

![interaction between C and ASM](images/lec13/interaction_between_C_and_ASM.png)

---

## Algorithm 

The lecture develops the following algorithm.
 
 Step 1 — Pass Initial Values

 Step 2 — Initialize Registers

 Step 3 — Store Final Count

 Step 4 — Perform Addition

 Step 5 — Increment Counter

 Step 6 — Loop Comparison


---

# Relationship Between C and Assembly

The lecture demonstrates practical:

- C-to-assembly interaction
- ABI-based communication
- register-based argument passing

This is an example where:

- high-level software
- low-level assembly
- ABI conventions

all interact together.

---

# Hardware Perspective

The assembly implementation directly maps to:

- register operations
- ALU additions
- branch comparisons
- loop execution
- register transfers

inside actual processor hardware.
The processor internally performs:

- register reads
- arithmetic operations
- comparison operations
- branching

according to ISA instructions.

---

## Key Takeaways

After this lecture, the learner understands:

- how ABI registers are practically used
- how arguments are passed to assembly functions
- how results are returned
- how loops are implemented in assembly logic
- how C interacts with assembly code

---


- ABI-based programming
- C and assembly interaction
- register-based function communication

inside RISC-V architecture.

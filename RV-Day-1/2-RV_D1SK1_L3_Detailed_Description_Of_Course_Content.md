## Overview

This lecture provides a detailed breakdown of the complete NASSCOM RISC-V based MYTH workshop structure.
It explains objectives of each workshop day, topics, the practical labs involved and the overall learning roadmap from software to hardware design
In simpler terms it is a roadmap to the course.

---

# Course Structure Overview

The MYTH workshop is divided into five major learning phases:

```text
Day 1 → RISC-V ISA and GNU Toolchain
Day 2 → ABI
Day 3 → Digital Logic with TL-Verilog and Makerchip
Day 4 → Basic RISC-V CPU Microarchitecture
Day 5 → Complete Pipelined RISC-V CPU
```

---

## Day 1 — RISC-V ISA and GNU Toolchain

Day 1 focuses on:

- introduction to RISC-V
- compiler flow
- software toolchain
- integer number representation

Topics covered:

- basic RISC-V terminology
- software-to-hardware flow
- GCC compilation
- signed and unsigned number systems

---

## Day 2 — ABI and Verification Flow

Day 2 introduces:

- Application Binary Interface (ABI)
- register conventions
- memory allocation

Topics covered:

- ABI fundamentals
- assembly function calls
- load/store operations
- register usage

The learner begins understanding how software interfaces with processor architecture.

---

## Day 3 — Digital Logic with TL-Verilog and Makerchip

Day 3 transitions into digital hardware design.

Major topics:

- combinational logic
- sequential logic
- pipelined logic
- validity concepts
- hierarchy

The lecture introduces:

- TL-Verilog
- Makerchip IDE
- timing abstraction
- pipeline stages

---

## Day 4 — Basic RISC-V CPU Microarchitecture

Day 4 focuses on building a simple RISC-V CPU.

Topics include:

- single-cycle CPU architecture
- program counter implementation
- instruction fetch logic
- decode logic
- register file
- ALU operations
- branch instructions
- testbench creation

The learner begins constructing actual processor hardware blocks.

---

## Day 5 — Complete Pipelined RISC-V CPU

Day 5 introduces:

- pipelining
- pipeline hazards
- forwarding
- load/store instructions
- complete CPU integration

Topics covered:

- control flow hazards
- RAW hazards
- branch correction
- ALU completion
- data memory integration
- jump instruction handling

The final outcome is a functioning pipelined RISC-V CPU.

---

# Learning Progression

The course follows a bottom-up approach:
```text
Software
    ↓
Assembly
    ↓
ISA
    ↓
Digital Logic
    ↓
CPU Datapath
    ↓
Pipeline Design
```

This progression helps learners understand:

- how software executes on hardware
- how processors are constructed
- how pipelining improves performance

---


# Notes

This lecture provides the roadmap for the entire MYTH workshop and helps learners understand how all future lectures connect together.

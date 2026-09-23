# 23-Timing

## Overview

This lecture introduces:
- pipeline logic
- timing abstraction
- multi-stage computations
- TL-Verilog pipelines
- stage boundaries
- pipeline retiming
- code reduction advantages
- timing vs functionality separation

The lecture demonstrates implementing Pythagoras theorem in hardware using pipelined computation stages. This lecture introduces pipelined hardware execution.

---

# Pythagoras Theorem Hardware Example

The computation implemented:
```text
c = sqrt{a^2 + b^2}
```
The lecture explains:

- square a
- square b
- add results
- compute square root

using hardware pipeline stages.
<img width="889" height="490" alt="image" src="https://github.com/user-attachments/assets/796c1730-ad55-4d0b-92a1-99c4bf806de6" />


<img width="889" height="490" alt="image" src="https://github.com/user-attachments/assets/a8bd2ff9-80e1-4cf7-a799-47cfcfab7ef0" />

## Deep Logic Problem

Modern processors run at gigahertz frequencies. Therefore too much logic cannot fit inside one clock cycle.

## Timing Violation Concept

if logic takes too long signals miss next clock edge. 
Meaning - timing failure occurs.

## Distributing Computation Across Cycles

The solution introduced is distributing this computation over multiple cycles. This is pipelining.

## Pipeline Stages

The lecture divides computation into stages:
| Stage   | Operation      |
| ------- | -------------- |
| Stage 1 | Square A and B |
| Stage 2 | Add results    |
| Stage 3 | Square root    |
Each stage is separated by flip-flops.



## Flip-Flop Between Stages

Intermediate values get captured in flip-flops after computation at each stage. Stage boundaries imply flip-flops automatically.

---

# Hardware Perspective

This lecture introduces pipelining. All high-performance CPUs fundamentally rely on:

- deep pipelining
- stage partitioning
- timing optimization
- register insertion

The lecture also introduces timing abstraction, which is a key productivity advantage of TL-Verilog hardware modeling.
<img width="889" height="490" alt="image" src="https://github.com/user-attachments/assets/70ade48f-7610-4b02-84c0-f78376d92288" />

---

# Key Takeaways

After this lecture, the learner understands:

- why pipelining is necessary
- logic depth limitations
- multi-stage computation
- stage boundaries

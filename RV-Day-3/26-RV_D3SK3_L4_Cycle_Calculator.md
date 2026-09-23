# 26-RV_D3SK3_L4_Cycle_Calculator

## Overview

This lecture extends the earlier sequential calculator and pipeline logic concepts to create a multi-cycle pipelined calculator. The lecture introduces:

- explicit pipelines
- pipeline stages
- retiming logic
- valid cycles
- invalid cycles
- two-cycle latency
- recirculation paths
- stage movement of multiplexers
- timing alignment
- iterative computation pipelines

The lecture demonstrates converting a single-cycle calculator into a two-cycle pipelined calculator.

---

# High Frequency Pipeline Motivation

In order to run this calculator in a high frequency circuit, one cycle may not be sufficient.

---

# Splitting Computation Across Cycles

The solution is to divide calculator operation across two pipeline stages.

---

# New Pipeline Structure

work is divided into:
| Stage   | Operation              |
| ------- | ---------------------- |
| Stage 1 | Arithmetic Computation |
| Stage 2 | Multiplexer Selection  |

## Multiplexer Retiming

Multiplexer is moved to a second pipeline stage.
Meaning - arithmetic is computed first and output selection is delayed by one cycle.

--- 

## Output Zeroing Logic

Output is driven with a zero value during:

- invalid cycles
- reset condition.


<img width="1853" height="961" alt="Image" src="https://github.com/user-attachments/assets/61340d53-0359-465d-b2c5-34502a0383a1" />

---

# Hardware Perspective

This lecture introduces several processor concepts: 

- multi-cycle execution
- staged arithmetic
- feedback latency
- valid signaling
- retiming
- iterative pipelines
- Computation latency changes feedback timing. As pipelines deepen recirculation paths require additional staging alignment.

---

# Key Takeaways

After this lecture, the learner understands:

- explicit pipeline declaration
- stage partitioning
- multi-cycle calculator design
- valid cycle generation
- oscillating one-bit counters
- two-cycle recirculation
- feedback latency
- mux retiming
- waveform verification
- timing-aware pipeline design

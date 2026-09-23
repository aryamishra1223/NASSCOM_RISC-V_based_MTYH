# 31-RV_D3SK4_L5_Calulator_Single_Value_Memory_Lab

## Introduction

The pipelined calculator by introducing single-value memory support. The calculator now supports:

- MEM operation
- RECALL operation

This lecture introduces:
- state update logic
- recirculating state paths
- memory retention
- memory recall
- multi-cycle recirculation
- explicit recirculation in TL-Verilog
- functional clock gating concepts
- state update multiplexers
- memory pipeline timing

The calculator evolves from a pure arithmetic pipeline into a stateful programmable calculator.

---

# Goal of the Lecture

The calculator will now store a computed value retrieve that stored value later.

---

# MEM and RECALL Operations

Two new operations:
| Operation | Purpose                         |
| --------- | ------------------------------- |
| MEM       | Store current value into memory |
| RECALL    | Retrieve stored memory value    |

---

# Hardware Perspective

| Concept                 | Meaning                            |
| ----------------------- | ---------------------------------- |
| Stateful Logic          | Hardware remembers previous values |
| Recirculation           | Feedback path preserves state      |
| Retain Case             | Preserve previous state            |
| Memory Update Mux       | Select next state value            |
| Functional Clock Gating | Avoid unnecessary updates          |
| Pipeline Cadence        | Timing alignment across stages     |
| Recall Path             | Reusing stored data                |

State is implemented using recirculation through flip-flops.

---
# Memory Update Cases

The memory supports three update cases.

## Case 1 — Reset

During reset memory becomes zero.

## Case 2 — Retain Existing Memory

If no MEM operation requested, then memory recirculates previous value. We take the value out of the memory and feed it back into the output value.

## Case 3 — Memory Store Operation

If we're doing a memory operation, then we want to grab the value of output and capture it in the memory. The memory captures output from two cycles ago.

<img width="1855" height="961" alt="Image" src="https://github.com/user-attachments/assets/29adce8e-59ad-4b9b-a038-2ec6d124a5ed" />

---

# Key Learning Outcome

After this lecture, the learner understands:

- stateful datapath design
- explicit state recirculation
- memory update logic

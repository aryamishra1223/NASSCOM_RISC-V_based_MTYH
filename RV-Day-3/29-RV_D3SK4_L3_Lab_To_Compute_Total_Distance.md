# 29-RV_D3SK4_L3_Lab_To_Compute_Total_Distance

## Introduction

This lecture extends the earlier Pythagorean theorem pipeline to create a total distance accumulator. The lecture introduces:

- state retention
- accumulation logic
- pipeline recirculation
- ahead operators
- validity-aware accumulation

---

# Stateful Logic

total distance is state.
Meaning - value must persist across cycles.

---

# Validity Interaction

The total distance is meaningful always. Unlike, temporary pipeline signals the accumulated total remains valid continuously.

---

# Outside Valid Condition

One needs to go outside of the valid condition because total distance must retain value even during invalid cycles.

---

# Reset Handling

Reset is propagated through the pipeline, i.e., it marches through the pipeline. This ensures all stages observe reset consistently. This establishes association between the global reset signal and the computation. Benefits:

- all state resets coherently
- all pipeline stages align
- transactions remain consistent

## Reset Transactions

A given transaction will be reset or not.

---

# Hardware Perspective

Pipeline state must remain consistent across transactions.

![Updated Waveform And Diagram](images/lec29/Updated_Waveform_And_Diagram.png)

---

# Key Learning Outcome

After this lecture, the learner understands:

- accumulation pipelines
- recirculating state
- previous transaction access
- ahead operators

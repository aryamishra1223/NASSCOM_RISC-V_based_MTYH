# 30-cycle_Calculator_with_Validity

## Introduction

This lecture upgrades the earlier pipelined calculator by replacing explicit output zeroing with validity-aware computation. The lecture also introduces:

- MakerChip visualization tools
- waveform debugging
- visualization-based learning
- calculator visualization

---

# Replacing Output Zeroing With Validity

Instead of now zeroing out the output value every other cycle, we use validity. We thus transition from manually masking outputs to validity-aware computation.

---

# Alternate-Cycle Calculator

Every other cycle we have valid input.
Meaning - calculations occur every alternate cycle. Intermediate cycles become invalid cycles.

---

# Valid Signal

The pipeline already contains valid signal which indicates whether computation is meaningful.

---

# Reset Interaction With Validity

We have to make sure the logic is valid during reset.

## Why Reset Must Be Valid

The calculator output recirculates back into input. Therefore reset must propagate correctly
through feedback path.

---

# Stateful Output

The output value is state because output feeds future computations.

---

# Valid-Or-Reset Signal

This signal enables logic during:
- reset
- - valid cycles.

---

# Garbage Values Are Acceptable

It's no longer necessary to explicitly zero out the output. Invalid cycles can safely contain:

- garbage values
- don't care values.




---

# Hardware Perspective

Invalid cycles do not require explicit output cleanup. Validity itself defines whether computation matters. This simplifies:

- datapath logic
- debugging
- waveform interpretation
- low-power design.

---

# Key Learning Outcome

After this lecture, the learner understands:

- validity-aware calculator design
- valid-when conditions
- reset-aware validity
- don't care propagation


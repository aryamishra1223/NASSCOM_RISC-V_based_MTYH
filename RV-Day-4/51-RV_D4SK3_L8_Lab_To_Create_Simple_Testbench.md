# 51-RV_D4SK3_L8_Lab_To_Create_Simple_Testbench

## Overview

This lecture implements a simple testbench validation mechanism for the RISC-V CPU using:
- `*passed`

signals in MakerChip. The lecture focuses on:

- simulation pass/fail signaling
- observing register values
- validating program correctness
- automatic simulation termination
- testbench-based verification

The testbench checks whether:
- register `x10`
contains the correct summation result.

---

# Register Monitoring

The testbench directly observes the register file entry:
- `x10`

which stores the accumulated sum.

---

# Delayed Pass Detection

The lecture uses ahead by five to:

- delay simulation termination
- allow additional waveform visibility.

---

<img width="1843" height="872" alt="Image" src="https://github.com/user-attachments/assets/feec3829-c6c0-4c9b-8ebd-a3c0b8c6786a" />

# Key Learning Outcome

After this lecture, the learner understands:

- MakerChip pass signaling

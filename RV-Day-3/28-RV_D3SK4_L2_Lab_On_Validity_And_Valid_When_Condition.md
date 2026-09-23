# 28-RV_D3SK4_L2_Lab_On_Validity_And_Valid_When_Condition

## Overview

This lecture demonstrates:
- practical usage of validity
- valid-when conditions
- pipeline validity propagation
- TL-Verilog syntax

---

## Dotted Line Visualization

The diagram uses dotted lines to represent valid conditions.

## Waveform Debugging

The instructor demonstrates:

- selecting signals
- observing pipeline flow
- tracing computations.

<img width="1853" height="961" alt="Image" src="https://github.com/user-attachments/assets/f5f0ab66-fe36-43f0-b96b-6b7bd97d52e2" />

<img width="827" height="659" alt="Image" src="https://github.com/user-attachments/assets/2a2185e4-9da1-44c8-9554-84883f3767d8" />

<img width="793" height="787" alt="Image" src="https://github.com/user-attachments/assets/8c0e3997-91f4-457c-88b0-831ea6c305d1" />

<img width="1855" height="961" alt="Image" src="https://github.com/user-attachments/assets/b21c5b65-a778-452f-bd76-acee1f6788c8" />

---

# Hardware Perspective

Validity controls whether state updates should occur. This is critical in:

- pipelines
- accumulators
- processors
- DSP systems
- low-power hardware

because invalid computations must not corrupt state.

---

# Key Takeaways

After this lecture, the learner understands:

- practical validity implementation
- valid-when syntax
- MakerChip random stimulus generation
- TL-Verilog file structure
- M4 preprocessing
- Nav-TLV interpretation
- accumulation datapaths
- validity-controlled state updates
- pipeline debugging
- waveform interpretation

This lecture transitions validity from theoretical abstraction to practical hardware implementation.

# 42-ISBUJ

## Overview

This lecture improves instruction field decode logic by introducing validity-aware field decoding
using when conditions. The lecture focuses on:

- conditional field validity
- valid decode signals
- instruction-type-aware decoding
- waveform cleanliness
- validity propagation
- decode correctness
- conditional field generation

This lecture applies TL-Verilog validity concepts to RISC-V instruction decode logic.

---

<img width="1851" height="826" alt="Image" src="https://github.com/user-attachments/assets/5fe33885-6b33-4631-9bb3-440254f1cac5" /> 
<img width="1855" height="954" alt="Image" src="https://github.com/user-attachments/assets/351fe365-75ab-4128-8781-825e7615f167" /> 
<img width="1855" height="954" alt="Image" src="https://github.com/user-attachments/assets/ae7c9d7a-9e0f-4e69-81bf-534127c4a9d4" /> 
<img width="1855" height="954" alt="Image" src="https://github.com/user-attachments/assets/cf0c2300-7ccc-4ff6-b23c-ca21fd4f5572" />

---

# Hardware Perspective

Decoded fields should only propagate when architecturally meaningful. This is fundamental to:

- clean pipelines
- correct control logic
- scalable CPU verification
- efficient hardware implementation

---

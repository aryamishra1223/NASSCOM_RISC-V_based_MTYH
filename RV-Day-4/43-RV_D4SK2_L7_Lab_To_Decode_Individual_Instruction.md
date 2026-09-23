## Overview

This lecture implements individual instruction decode logic for the RISC-V CPU. The lecture focuses on:

- instruction-specific decode signals
- funct7/funct3/opcode matching
- decode bit vectors
- wildcard decoding
- branch instruction decoding
- instruction classification
- Verilog `==?` operator
- don't care bits

This lecture is the point where the CPU begins identifying exact instructions instead of only instruction types.

---

# Starting With Test Program Instructions

We're going to start by just decoding the instructions that are relevant to our particular test program.

---

# Initial Instructions To Decode

The ones circled in red are the initial instructions to decode:

![Exact Instruction Decode](images/lec43/Exact_Instruction_Decode.png)

---

# Decode Vector Formula

Combined decode vector:
```text
$dec_bits[16:0] = {$funct7, $funct3, $opcode};
```

## Why Combine Decode Fields?

This simplifies instruction matching. Instead of multiple comparisons, the CPU performs one large pattern match.

---
<img width="1855" height="954" alt="Image" src="https://github.com/user-attachments/assets/351fe365-75ab-4128-8781-825e7615f167" />

# ADDI Instruction

For the ADDI instruction:
```text
Result = Source1 + Immediate
```
The ADDI operation uses:

- source operand from RS1
- immediate operand

to produce the final ALU result.

---

# ADD Instruction

The ADD instruction is very similar to ADDI except that both operands come from registers.
```text
Result = Source1 + Source2
```

---

# BLT Instruction

The BLT (Branch Less Than) instruction:

- does not produce a destination result
- does not write into the register file

Therefore no ALU result assignment is required for BLT at this stage.

---

# ALU Datapath

The datapath now becomes:
```text
Instruction →
Decode →
Register File →
ALU →
Result
```

---

# Hardware Perspective

The ALU is the execution engine of the processor datapath. It performs arithmetic and logical computations based on the decoded instruction. The ALU structurally behaves like multiple parallel computations followed by mux-based result selection.

---
<img width="1837" height="965" alt="Image" src="https://github.com/user-attachments/assets/4c11a724-33b3-4369-8631-6fbfef5ed28c" />

<img width="1855" height="954" alt="Image" src="https://github.com/user-attachments/assets/cf0c2300-7ccc-4ff6-b23c-ca21fd4f5572" />

# Key Learning Outcome

After this lecture, the learner understands:

- ALU implementation
- ternary-operator-based ALU selection
- ADD instruction execution

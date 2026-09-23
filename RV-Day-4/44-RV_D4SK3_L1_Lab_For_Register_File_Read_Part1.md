# Register File

Register file infrastructure already exists inside the provided shell. The register file is available
through a macro instantiation.

## Register File Capabilities

Capable of performing two reads in a cycle and one write.

## Register File Port Structure

The register file contains:
| Port Type   | Count |
| ----------- | ----- |
| Read Ports  | 2     |
| Write Ports | 1     |

## Why Two Reads?

Most RISC-V instructions require two source operands.
Examples:
```text
ADD rs1, rs2
SUB rs1, rs2
BEQ rs1, rs2
```

---

<img width="1855" height="954" alt="Image" src="https://github.com/user-attachments/assets/cf0c2300-7ccc-4ff6-b23c-ca21fd4f5572" /> 

---
# Key Learning Outcome

After this lecture, the learner understands:

    register file interfaces
    dual-read architectures
    register addressing
    read enable logic
    operand fetch


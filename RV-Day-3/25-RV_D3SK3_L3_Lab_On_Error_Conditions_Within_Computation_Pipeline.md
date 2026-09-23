# 25-RV_D3SK3_L3_Lab_On_Error_Conditions_Within_Computation_Pipeline

## Overview

This lecture discusses:
- TL-Verilog naming syntax
- pipeline signal naming rules
- MakerChip lab submission workflow
- sandbox cloning
- pipeline error aggregation logic
- multi-stage error propagation

---
## Pipe Signal Naming

Pipe signals begin with dollar sign ($)
Example:
```text
$signal_name
```

## Token-Based Naming

Identifiers are composed of tokens.
Example:
```text
$pipe_signal
```
where pipe and signal are individual tokens.

## Underscore Delimitation

The instructor explains lowercase pipe signals use underscore separation.
Example:
```text
$data_value
```

## Naming Styles in TL-Verilog

The lecture introduces three naming styles:
| Style                      | Meaning                |
| -------------------------- | ---------------------- |
| lowercase_with_underscores | Pipe signals           |
| PascalCase                 | State signals          |
| UPPERCASE_WITH_UNDERSCORES |  Keywords              |

## umbers in Identifiers

Numbers are allowed only at end of tokens.
Valid example:
```text
base64
```
---
## Fibonacci series in pipeline

 <img width="889" height="490" alt="image" src="https://github.com/user-attachments/assets/0b2e0cf1-4dce-40bd-9555-d3f8a235073b" />


# Hardware Perspective

This lecture combines TL-Verilog syntax
with real hardware pipeline concepts. The pipeline lab models distributed error handling which is extremely common in:

- CPUs
- DSP pipelines
- floating-point units
- ALUs
- memory systems

where error/status signals propagate across stages.

---

# Key Takeaways

After this lecture, the learner understands:

- TL-Verilog naming rules
- pipe signal syntax
- timing abstraction
- explicit pipelines
- default pipelines
- MakerChip cloning workflow
- multi-stage error propagation
- OR-based error aggregation
- staged error handling

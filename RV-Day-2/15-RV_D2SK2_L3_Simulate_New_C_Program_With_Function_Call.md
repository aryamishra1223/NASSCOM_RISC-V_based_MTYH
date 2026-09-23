# 15-RV_D2SK2_L3_Simulate_New_C_Program_With_Function_Call

## Introduction

The lecture demonstrates:
- viewing source files
- compiling C and ASM together
- executing using Spike
- disassembling executable code
- observing ABI register passing
- 
---

## Main C Program

The lecture explains that the main C program:

- performs the function call
- passes arguments
- receives return value

---

## Function Declaration

The lecture points out that:

- function definition exists in C
- actual implementation exists in assembly

---

## Viewing the Assembly File

The assembly file:
```text
load.s
```
contains:

- assembly implementation
- loop logic
- ABI register operations

---

## Assembly Directives

The lecture briefly discusses:
```text
.text
```
The instructor explains:
```text
After compilation they should go under the text section.
```
This means that the executable instructions go into the text/code segment.

![load.S](images/lec15/load.S.png)

---

## Compilation Process

The lecture recompiles the program using:
```text
riscv64-unknown-elf-gcc -Ofast -mabi=lp64 -march=rv64i -o 1to9_custom.o 1to9_custom.c load.S
```
Important Compiler Options
| Option            | Meaning            |
| ----------------- | ------------------ |
| `-Ofast`          | Optimization level |
| `-mabi=lp64`      | ABI selection      |
| `-march=rv64i`    | RV64I architecture |
| `-o`              | Output executable  |

We must make sure we are in the same directory where our files are because compiler must access the C file and the ASM file together.

---


# Disassembly of Executable

The lecture then disassembles the executable using:
```text
riscv64-unknown-elf-objdump -d 1to9_custom.o
```
The output is piped using:
```text
| less
```
to scroll through instructions.

![Objdump Disassembly](images/lec15/Objdump_Disassembly.png)

---

# ABI Argument Passing

Variables are passed through a1 and a0 only. The instructor says that these are ISA specifications.

---

# Relationship Between C and Assembly

The lecture demonstrates:

- C calling assembly
- assembly returning values
- ABI-based communication

The load function performs computations and returns result through a0 back to the main C program.

---

# Hardware Perspective

The lecture directly demonstrates:

- software compilation
- executable generation
- function jumps
- register-based communication
- instruction disassembly

which correspond to:

- instruction fetch
- branch execution
- register access
- function transfer

inside actual processor hardware.

---

# Key Takeaways

- how C and Assembly interact
- how ABI argument passing works
- how functions jump between files
- how to compile mixed C/ASM programs
- how to simulate using Spike
- how to analyze disassembly output


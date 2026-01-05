<div align="center">

# ⚙️ **CESSER**
### 16-bit CPU Emulator & Mini Assembler (Pascal)

Low-level • Educational • Stack-based • ISA Emulator

![Language](https://img.shields.io/badge/Language-Pascal-blue)
![Architecture](https://img.shields.io/badge/Architecture-16--bit-orange)
![Emulator](https://img.shields.io/badge/Type-CPU%20Emulator-purple)
![Assembler](https://img.shields.io/badge/Includes-Assembler-green)
![License](https://img.shields.io/badge/License-MIT-black)

</div>

---

## 📌 Overview

**CESSER** (**C**ustom **E**mulated **S**tack-based **S**ystem **E**xecute**R**)  
is a **16-bit CPU emulator** written in **FreePascal**, complete with a **mini assembler**, **RAM**, **stack**, and **subroutine support**.

This project simulates how a real processor works internally — from **instruction decoding**, **register manipulation**, **stack operations**, to **program execution**.

CESSER is built for **learning low-level systems**, **computer architecture**, and **emulator design**.

---

## ✨ Features

✅ 16-bit Virtual CPU  
✅ Custom Instruction Set Architecture (ISA)  
✅ Built-in Mini Assembler  
✅ 4KB RAM Memory  
✅ Stack Pointer & Subroutines (`CALL` / `RET`)  
✅ Conditional Jumps (`JZ`, `JNZ`)  
✅ Arithmetic Instructions  
✅ Interactive CLI Emulator  

---

## 🧠 CPU Architecture

```
┌─────────────────────────────┐
│           CESSER CPU        │
├──────────────┬──────────────┤
│ Registers    │ R0 R1 R2 R3  │
│              │ SP PC STATUS │
├──────────────┴──────────────┤
│ RAM          │ 4 KB (Word)  │
├─────────────────────────────┤
│ Stack        │ Grows Down   │
├─────────────────────────────┤
│ ISA          │ Custom       │
└─────────────────────────────┘
```

---

## 🧱 Instruction Set (ISA)

| Instruction | Description |
|-------------|------------|
| `MOV` | Move data |
| `ADD` | Addition |
| `SUB` | Subtraction |
| `MUL` | Multiplication |
| `CMP` | Compare values |
| `LOAD` | Load from memory |
| `STORE` | Store to memory |
| `JMP` | Unconditional jump |
| `JZ` | Jump if zero |
| `JNZ` | Jump if not zero |
| `CALL` | Call subroutine |
| `RET` | Return from subroutine |
| `PUSH` | Push to stack |
| `POP` | Pop from stack |
| `PRINT` | Debug output |
| `HALT` | Stop execution |

---

## 📂 Project Structure

```
CESSER/
└── PROCESSER/
    └── cesser.pas   # CPU Emulator + Assembler + VM
```

---

## 🔄 Execution Flow

```
Assembly Code
     ↓
Mini Assembler
     ↓
Bytecode in RAM
     ↓
Fetch → Decode → Execute
     ↓
CPU Registers & Memory Updated
```

---

## 🚀 Getting Started

### 🔧 Requirements

- FreePascal Compiler (FPC)
- Terminal / Command Prompt

---

### ⚙️ Compile

```bash
fpc cesser.pas
```

---

### ▶ Run

```bash
./cesser
```

---

## 🖥️ Emulator Commands

| Command | Description |
|-------|------------|
| `load <file>` | Assemble & load program |
| `run` | Start CPU execution |
| `reset` | Reset CPU state |
| `help` | Show help |
| `quit` | Exit emulator |

---

## 🧪 Example Assembly Program

```asm
; Factorial of 5
MOV R0, 5
MOV R1, 1
CALL 20
JMP 30

20:
CMP R0, 1
JZ 25
MUL R1, R0
SUB R0, 1
JMP 20

25:
RET

30:
PRINT R1
HALT
```

Expected output:
```
[CPU OUT] R1 = 120
```

---

## 🧵 Stack & Subroutines

CESSER implements a **real stack model**:

- `CALL` pushes return address to stack
- `RET` pops address back into `PC`
- `PUSH` / `POP` manipulate stack directly

This allows **modular programs**, **loops**, and **function-like behavior**.

---

## 🎯 Learning Outcomes

By building and using **CESSER**, you learn:

- How CPUs fetch & execute instructions
- Register-based computation
- Stack memory mechanics
- Assembly-level program flow
- Emulator & VM architecture
- Low-level systems programming

---

## ⚠️ Notes

- This project is **educational**
- Instruction encoding is simplified
- Label handling is minimal
- Designed for clarity, not performance

---

## 📜 License

MIT License — free to use, modify, and learn from.

---

<div align="center">

**Developed by [norct](https://github.com/Unjou) 👾** 

</div>

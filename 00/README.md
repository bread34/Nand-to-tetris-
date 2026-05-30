# Nand2Tetris Project 1 — Boolean Logic

> Building a complete hierarchy of logic gates and combinational chips from a single primitive: **NAND**

## Overview

This repository contains my implementation of **Project 1: Boolean Logic** from the acclaimed **Nand2Tetris** course.

The objective of this project is to construct a complete set of fundamental logic gates and combinational hardware components using **only the NAND gate** as the elementary building block. By progressively combining previously constructed chips, increasingly complex digital circuits are created, demonstrating how modern computer hardware can emerge from a single universal logic gate.

This project serves as the first step toward building an entire computer system from the ground up, following the bottom-up hardware design philosophy of Nand2Tetris.

---

## Project Goals

* Understand the foundations of digital logic design.
* Learn how complex hardware emerges from simple primitives.
* Implement a hierarchy of reusable hardware components.
* Gain practical experience with Hardware Description Language (HDL).
* Develop intuition for computer architecture at the gate level.

---

## Core Philosophy

A central principle of this project is that **every chip is ultimately constructed from the NAND gate**.

The NAND gate is functionally complete, meaning that any Boolean function can be implemented using NAND gates alone.

Following the Nand2Tetris methodology:

1. Start with the primitive NAND gate.
2. Build basic logic gates.
3. Use those gates to construct more advanced components.
4. Continue composing chips into increasingly sophisticated hardware.

This demonstrates one of the most elegant concepts in computer engineering:

> Entire computer systems can be built from a single universal logic gate.

---

## Implemented Chips

### Basic Logic Gates

| Chip | Description         |
| ---- | ------------------- |
| Not  | Logical negation    |
| And  | Logical conjunction |
| Or   | Logical disjunction |
| Xor  | Exclusive OR        |
| Mux  | Multiplexer         |
| DMux | Demultiplexer       |

### Multi-Bit Gates

| Chip  | Description        |
| ----- | ------------------ |
| Not16 | 16-bit bitwise NOT |
| And16 | 16-bit bitwise AND |
| Or16  | 16-bit bitwise OR  |
| Mux16 | 16-bit multiplexer |

### Multi-Way Components

| Chip      | Description                  |
| --------- | ---------------------------- |
| Or8Way    | OR reduction across 8 inputs |
| Mux4Way16 | 4-way 16-bit multiplexer     |
| Mux8Way16 | 8-way 16-bit multiplexer     |
| DMux4Way  | 4-way demultiplexer          |
| DMux8Way  | 8-way demultiplexer          |

---

## Project Structure

```text
./
│
├── Not.hdl
├── And.hdl
├── Or.hdl
├── Xor.hdl
├── Mux.hdl
├── DMux.hdl
│
├── Not16.hdl
├── And16.hdl
├── Or16.hdl
├── Mux16.hdl
│
├── Or8Way.hdl
├── Mux4Way16.hdl
├── Mux8Way16.hdl
├── DMux4Way.hdl
├── DMux8Way.hdl
│
├── *.tst
├── *.cmp
│
└── README.md
```

---

## Design Approach

The implementation follows a hierarchical hardware design methodology.

### Layer 1 — Primitive Component

```text
NAND
```

### Layer 2 — Elementary Gates

```text
NAND
 ├── Not
 ├── And
 └── Or
```

### Layer 3 — Intermediate Components

```text
Not
And
Or
 ├── Xor
 ├── Mux
 └── DMux
```

### Layer 4 — Multi-Bit Chips

```text
And16
Or16
Not16
Mux16
```

### Layer 5 — Multi-Way Chips

```text
Or8Way
Mux4Way16
Mux8Way16
DMux4Way
DMux8Way
```

Each chip was built using previously verified components, creating a clean and reusable hardware abstraction hierarchy.

---

## Verification

All chips were tested using the official Nand2Tetris hardware simulator and the provided test scripts.

Verification included:

* Functional correctness
* Truth table validation
* Multi-bit operations
* Multi-way routing behavior
* Edge-case testing

Each implementation successfully passes the corresponding `.tst` and `.cmp` validation files.

---

## Technologies Used

* Hardware Description Language (HDL)
* Nand2Tetris Hardware Simulator
* Boolean Algebra
* Digital Logic Design Principles

---

## Key Concepts Learned

Through this project, I developed practical understanding of:

* Boolean logic
* Logic gate construction
* Functional completeness of NAND
* Combinational circuit design
* Multiplexing and demultiplexing
* Hardware abstraction
* Hierarchical system design
* Digital computer foundations

---

## Why This Project Matters

Most programmers interact with computers at a high level through programming languages and software frameworks.

This project explores the opposite direction:

**How does hardware itself emerge?**

By building every component from NAND gates alone, this project reveals the layers of abstraction that ultimately lead to CPUs, memory systems, operating systems, and modern software.

It provides a rare opportunity to understand computing from the transistor-inspired logic level upward.

---

## Course Reference

This project is part of the Nand2Tetris curriculum:

**From NAND Gates to a Modern Computer**

Developed by:

* Noam Nisan
* Shimon Schocken

The course guides students through building an entire computer system and software stack from first principles.

---

## Future Work

Upcoming projects in the Nand2Tetris journey include:

* Sequential Logic
* Memory Components
* Arithmetic Logic Unit (ALU)
* CPU Design
* Machine Language
* Assembler
* Virtual Machine
* Compiler
* Operating System

The long-term goal is to build a complete working computer system from the ground up.

---

## Author

Computer Engineering / Systems Enthusiast

Passionate about understanding computers at the lowest levels of abstraction and exploring how complex systems emerge from simple building blocks.

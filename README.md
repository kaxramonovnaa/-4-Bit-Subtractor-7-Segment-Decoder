# Digital Logic Design: 4-Bit Subtractor & 7-Segment Decoder

## 📌 Project Overview

This project focuses on designing and implementing two digital logic circuits:

- **4-Bit Binary Subtractor** – Performs subtraction of two 4-bit binary numbers using Full Adders and two's complement arithmetic.
- **7-Segment Decoder** – Converts a 4-bit binary input into signals that control a 7-segment display, supporting hexadecimal digits (0–F).

The circuits were designed using Boolean algebra, truth tables, Karnaugh maps (K-maps), and basic logic gates.

## ⚙️ Project Components

### 1. 4-Bit Subtractor

The subtractor performs binary subtraction using the following principle:

\[
A-B=A+\overline{B}+1
\]

**Implementation:**
- Four 1-bit Full Adders connected in series.
- NOT gates to invert every bit of B.
- Initial carry input (Cin) set to 1.
- Carry output (Cout) connected to the next Full Adder.

**Full Adder Boolean Expressions:**

- Sum: `S = A XOR B XOR Cin`
- Carry: `Cout = A·B + Cin·(A XOR B)`

**Simulation Examples:**

| Operation | Result |
|---|---|
| 6 - 2 | 4 |
| 5 - 7 | E |
| 9 - 3 | 6 |

Three hexadecimal displays are used to show A, B, and the subtraction result.

### 2. 7-Segment Decoder

The decoder receives a 4-bit binary input (D3, D2, D1, D0) and generates seven output signals (Sa–Sg).

**Design Process:**

1. Created a truth table for hexadecimal digits 0–F.
2. Used Karnaugh maps to simplify Boolean expressions for segments Sa and Sb.
3. Derived minimized Boolean expressions using Sum of Products (SOP).
4. Implemented the logic circuit using NOT, AND, and OR gates in Digital.

**Boolean Expressions:**

**Segment Sa:**
```text
D2'D0' + D3'D1 + D2D1 + D3'D2D0
+ D3D2'D1' + D3D2D0'
```

**Segment Sb:**
```text
D2'D1' + D2'D0' + D3'D1D0
+ D3'D1'D0' + D3D1'D0
```

The decoder uses active-high outputs, where `1 = ON`.

## 🧪 Verification & Testing

The circuits were verified through simulation.

- Subtractor test: `6 - 2 = 4`
- Additional subtraction tests: `5 - 7 = E` and `9 - 3 = 6`.
- Decoder verification: Matches the truth table for all 16 possible inputs (0000–1111).

## 🛠️ Concepts & Technologies

- Digital Logic Design
- Boolean Algebra
- Binary Arithmetic
- Full Adders
- Two's Complement
- Truth Tables
- Karnaugh Maps (K-maps)
- Sum of Products (SOP)
- Logic Gates (NOT, AND, OR, XOR)
- Digital Logic Simulator

## 🎯 Learning Outcomes

Through this project, I practiced:

- Designing combinational logic circuits.
- Understanding and implementing Full Adders.
- Building a multi-bit subtractor using two's complement.
- Simplifying Boolean expressions using Karnaugh maps.
- Designing hexadecimal 7-segment decoders.
- Testing and verifying digital circuits through simulation.

## 📄 Project Documentation

The project documentation includes:
- Design methodology
- Truth tables
- Boolean expressions
- Logic circuit design
- Simulation results

---

**Course:** Digital Logic Design  
**Project:** 4-Bit Subtractor & 7-Segment Decoder

# 4-bit ALU Design (CircuitVerse)

This project implements a 4-bit Arithmetic Logic Unit (ALU) designed and simulated in [CircuitVerse](https://circuitverse.org).  
It was created for the CS211: Computer Architecture course at Rutgers University (Spring 2025).

**Live Project**: [View in CircuitVerse](https://circuitverse.org/simulator/embed/untitled-da3a4770-a9ea-404f-b584-227d41c55722)

---

## Description

The ALU supports five operations controlled by a 3-bit OpCode:

| OpCode | Operation | Description              |
|--------|-----------|--------------------------|
| 000    | ADD       | A + B                    |
| 001    | SUBTRACT  | A - B (2’s complement)   |
| 010    | AND       | Bitwise AND              |
| 011    | OR        | Bitwise OR               |
| 100    | SLT       | Output 0001 if A < B     |

---

## Subcircuits

- `Adder`: 4-bit ripple-carry adder (built from Full Adders)
- `Subtractor`: Uses inverted B and Cin=1 for A - B
- `AND`, `OR`: 4-bit bitwise logic
- `Comparator`: Set-less-than logic using sign bit
- `ALU`: Main unit selects result via multiplexer and sets flags

---

## Flags

- `Negative`: Set if MSB of result is 1
- `Carry`: Adder/Subtractor carry-out
- `Overflow`: XOR of last two carries

---

## Tools

- CircuitVerse.org (simulator)
- Manual logic gate design (no built-in arithmetic blocks)

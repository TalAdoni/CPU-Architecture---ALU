# Lab 1: ALU Implementation in VHDL

This project implements an Arithmetic Logic Unit (ALU) using three units: Shifter, Boolean, and Arithmetic.

The system supports three operation codes:

01 - Arithmetic:
- 01000: result = Y + X
- 01001: result = Y - X
- 01010: result = -X

10 - Shifter:
- 10000: result is shift Y left by k X LSB's
- 10001: result is shift Y right by k X LSB's

11 - Boolean:
- 11000: NOT Y
- 11001: X OR Y
- 11010: X AND Y
- 11011: X XOR Y
- 11100: X NOR Y
- 11101: X NAND Y
- 11111: X XNOR Y

### Inputs:
- `X` signal
- `Y` signal
- `ALUFN` control signal where ALUFN[4:3] choose the selected module (01 -> AdderSub, 10 -> Shifter, 11 -> Logic), and each module acts differently with control of ALUFN[2:0].

### Outputs:
- FLAGS: Zero, Carry, Negative, Overflow.
- ALUout: The system output according to the selected module.

The lab was created by Omri Aviram and Tal Adoni.

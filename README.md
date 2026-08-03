# Full Adder using Verilog

## Overview
This project implements a **1-bit Full Adder** using Verilog HDL.

A Full Adder adds three binary inputs:
- A
- B
- Cin (Carry Input)

It produces:
- Sum
- Cout (Carry Output)

## Truth Table

| A | B | Cin | Sum | Cout |
|---|---|-----|-----|------|
|0|0|0|0|0|
|0|0|1|1|0|
|0|1|0|1|0|
|0|1|1|0|1|
|1|0|0|1|0|
|1|0|1|0|1|
|1|1|0|0|1|
|1|1|1|1|1|

## Logic Equations

Sum = A ⊕ B ⊕ Cin

Cout = (A & B) | (B & Cin) | (A & Cin)

## Files

- full_adder.v → Verilog source
- full_adder_tb.v → Testbench
- simulation.png → Simulation waveform

## Tools Used

- Icarus Verilog
- GTKWave
- ModelSim / Vivado (Optional)

## Simulation

Compile:

```bash
iverilog -o fulladder full_adder.v full_adder_tb.v
```

Run:

```bash
vvp fulladder
```

Generate waveform:

```bash
gtkwave fulladder.vcd
```

## Author

Your Name
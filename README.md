# Simple-Computer Simulator

A modular, educational computer architecture built in Logisim-Evolution.

## Description

This project simlulates a complete computer system with custom CPU, memory, and I/O components using Logisim-Evolution. Designed for computer architecture education, it demonstrates how basic operations are performed at the hardware level.

## Key Features:
- 8-bit RISC-style processor with 12-instruction ISA
- Modular design (CPU, RAM, ROM, and I/O in seperate circuits
- Comes with 3 verified example programs
- Visual debugging with clock-stepping

## Installation

### Requirements

Logisim-Evolution v3.8.0+

### Steps

1. Clone the repositiory
   git clone https://github.com/Swolisa/Simple-Computer.git
2. Open in Logisim-Evolution:
   File -> Open -> Select RSC.circ

### Usage
- Running Progrms
  1. Load bytecode into ROM (copy form program*_bytecode.txt)
  2. Control simulation:
     - Ctrl+K : Single clock tick
     - Ctrl+T : Continous clock
     - Ctrl+R : Reset
- Example Program (program1.txt)
  ; Subtract two values
  JMP start
  var1: A
  var2: F
  start:
  LDAC var1    ; Load 0xA
  MVAC         ; Move to R
  LDAC var2    ; Load 0xF
  SUB          ; A - F = -5 (0xFB)
  OUT
  HALT

  Expected output: 0xFB (shown on output register
  Full programs:
  - program2.txt (advanced arthrimetic/logic)
  - program3.txt (Loop demonstration)

## Contributing
We welcome contributions for your own purposes but the project is finsihed on in terms of my involvment for now.

## Authors and Acknowledgment
Author: Noah Brown
Special thanks to:
- Logisim-Evolution maintainers
- Middle Tennessee State University Assembly course

## License
MIT - Noah Brown 2024

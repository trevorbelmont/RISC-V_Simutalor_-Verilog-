# RISC-V Monocycle Processor Simulator

This repository contains a **RISC-V monocycle processor simulator** implemented in Verilog and executed in a **Jupyter Notebook on Google Colab**. The processor follows the standard RISC-V architecture and includes a **complete datapath** for executing instructions.

## Features
- **Full instruction execution pipeline** in a single cycle
- **Datapath implementation** including register file, ALU, memory, and control units
- **Binary instruction input** in **hex dump format**
- **Compatible with Assembly programs generated using Venus**
- **Generates animations of the datapath execution at the end of the simulation**

## Usage

To run the simulator, open the Jupyter Notebook in **Google Colab** and execute the provided cells.

### Input Format
The processor receives a **hex dump file** containing binary instructions. This dump can be generated from an **Assembly program** using the [Venus RISC-V Simulator](https://venus.cs61c.org/). The hex dump format is used for convenience in loading machine code directly into the processor's instruction memory.

### Example
To generate a hex dump from Venus:
1. Write and assemble your RISC-V Assembly code.
2. Export the binary in hexadecimal format.
3. Use this hex dump as input to the simulator.

## Datapath Overview
The **datapath** of this RISC-V processor includes:
- **Instruction Fetch (IF)**: Loads instructions from memory.
- **Instruction Decode (ID)**: Reads registers and decodes the instruction.
- **Execution (EX)**: Performs arithmetic or logic operations.
- **Memory Access (MEM)**: Loads/stores data if needed.
- **Write-back (WB)**: Updates register values.

Each instruction completes in a single cycle, making it a **monocycle implementation**.

### Datapath Animation
At the end of execution, the simulator generates **animated visualizations of the datapath**, illustrating how instructions move through the processor.

## Running in Google Colab
Simply open the notebook in **Google Colab**, upload your hex dump file, and run the simulation.

https://colab.research.google.com/drive/1T0hs4dQUmbr1k2FAl3bpXoldnj05oFPE?usp=sharing

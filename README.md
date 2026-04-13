📌 Overview

This project presents the design and FPGA implementation of an 8-bit ripple carry adder. The design was initially modeled in Simulink and converted into synthesizable Verilog using HDL Coder, followed by synthesis and implementation on FPGA.

The focus of this work is on hardware-oriented design, RTL implementation, and FPGA deployment, making it suitable for digital design and VLSI roles.

🧠 Design Description

The adder is implemented using a bitwise ripple carry architecture, where each bit performs full-adder logic:

Sum: sum[i] = a[i] ⊕ b[i] ⊕ carry[i]
Carry: carry[i+1] = (a[i] & b[i]) | (b[i] & carry[i]) | (a[i] & carry[i])

This structure is simple, scalable, and widely used in digital systems.

🏗️ Project Flow
🔹 1. Simulink Modeling
Designed adder using HDL-compatible blocks
Used fixed-point representation for hardware compatibility
Verified functionality through simulation
🔹 2. HDL Generation
Generated synthesizable Verilog using HDL Coder
Refined RTL for efficient FPGA implementation
🔹 3. FPGA Implementation
Imported RTL into Vivado
Created top-level module with clock-driven inputs
Applied timing constraints and resolved synthesis/placement issues
Successfully generated bitstream

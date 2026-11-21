<!---

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works
This project implements an 8-bit ripple carry adder (`tt_um_8bitadder`) for Tiny Tapeout. It takes two 8-bit input operands (`A` connected to `ui_in[7:0]` and `B` connected to `uio_in[7:0]`, with `uio` configured as inputs via `uio_oe`) and computes their sum onto the 8-bit dedicated output bus `uo_out[7:0]`. Since it is a combinational adder in this design, `clk`, `rst_n`, and `ena` are not actively used for sequential state.

## How to test

Apply test values to the two 8-bit inputs (`ui_in[7:0]` for operand A and `uio_in[7:0]` for operand B) and observe the resulting 8-bit sum on `uo_out[7:0]`. You can verify edge cases such as zero inputs, mid-range additions, and overflow wrap-around across the 8 output bits using the project testbench or hardware/simulation setup.

## External hardware

None required. This design uses only the standard Tiny Tapeout inputs and outputs without external PMODs or peripherals.

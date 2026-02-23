---
tags:
  - info
  - books
  - operating_systems
---
We can build a two-input `OR` gate. Each `NAND` gate in this setup represents a one-bit input of the entire `OR` gate.

2-bit `OR` gate logic diagram, built using 3 `NAND` gates with 4 pins just for 2 bits of input:
![[Pasted image 20260210193602.png]]

Configuration of the chip where the pins `3A` and `3B` take the values from `2Y` and `1Y`:
![[Pasted image 20260210194042.png]]

Truth table:

| A   | B   | C   | D   | Y   |
| --- | --- | --- | --- | --- |
| 0   | 0   | 1   | 1   | 0   |
| 0   | 1   | 1   | 0   | 1   |
| 1   | 0   | 0   | 1   | 1   |
| 1   | 1   | 0   | 0   | 1   |
To build an `OR` that operates on two 4-bit inputs, we need a total of four 74HC00 chips configured as `OR` gates, packaged as a simple chip:

(diagram error: it should have been `A1` on the input pin `1B`)
![[Pasted image 20260210195311.png]]
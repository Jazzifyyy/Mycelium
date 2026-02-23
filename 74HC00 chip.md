---
tags:
  - books
  - operating_systems
  - info
---
The 74HC00 is a chip with four 2-input `NAND` gates. The chip comes with 8 input pins and 4 output pins, 1 pin for connecting to a voltage source and 1 pin for connecting to the ground.

This device is the physical implementation of `NAND` gates that we can physically touch and use. But instead of just a single gate, the chip comes with 4 gates that can be combined (we can write the output of 1 `NAND` gate to an input of another `NAND` gate, thus chaining `NAND` gates together). Each combination enables a different logic function, effectively creating other logic gates. This feature is what makes the chip popular.

Logic diagram of 74HC00:
![[Pasted image 20260131184550.png]]

A user can use [[74HC00 chip]] without knowing its internals, but only the interface for using the device.

The layout of the device is:

![[Pasted image 20260131190045.png]]
The functionality of the pins are given in the following table:


| __Symbol__ | __Pin__ | __Description__ |
| ---------- | ------- | --------------- |
| 1A         | 1       | data input      |
| 2A         | 4       | data input      |
| 3A         | 9       | data input      |
| 4A         | 12      | data input      |
| 1B         | 2       | data input      |
| 2B         | 5       | data input      |
| 3B         | 10      | data input      |
| 4B         | 13      | data input      |
| 1Y         | 3       | data output     |
| 2Y         | 6       | data output     |
| 3Y         | 8       | data output     |
| 4Y         | 11      | data output     |
| GND        | 7       | ground (0 V)    |
| V_cc       | 14      | supply voltage  |
Functional description of the pins:


| __Input__ | Input  | Output |
| --------- | ------ | ------ |
| __nA__    | __nB__ | __nY__ |
| L         | X      | H      |
| X         | L      | H      |
| H         | H      | L      |
where $n \in \{ 1,2,3,4 \}$ is a number and H denotes HIGH voltage level, L denotes LOW voltage level, and X denotes "don't care".

When left as is, the 74HC00 is simply a `NAND` device with two 4-bit inputs.

Example:

![[Pasted image 20260210194650.png]]

![[Pasted image 20260210194719.png]]

# Also See:
+ [[building an OR gate using the 74HC00 chip]]
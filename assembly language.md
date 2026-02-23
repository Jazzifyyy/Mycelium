---
tags:
  - info
  - books
  - operating_systems
---
Assembly language is just the symbolic representation of [[machine language]] - by giving bit patterns mnemonic names.

This is a vast improvement when programmers had to write `0`s and `1`s. For instance, instead of writing `000000101`, a programmer can simply write `hlt` to stop the computer.

Example:

```asm
nand <op1>, <op2>
or <op1>, <op2>
```

The first line is equivalent to passing two 4-bit operands through a `NAND` gate: this corresponds to a single [[74HC00 chip]] left as is.

The second line is equivalent to passing two 4-bit operands through an `OR` gate:
this corresponds to a 4-input device built from 4 74HC00 chips. (See: [[building an OR gate using the 74HC00 chip]])
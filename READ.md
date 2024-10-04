
# Half Adder Verilog Module

This project contains a Verilog implementation of a half adder, which is a basic digital circuit used in binary addition. The half adder takes two single-bit inputs (`a` and `b`) and generates two outputs: the sum (`s`) and the carry (`c`).

## Code Overview

The module is defined with two inputs (`a` and `b`) and two outputs (`s` and `c`):

- `s`: The sum output, representing the XOR of the two inputs (`a ^ b`).
- `c`: The carry output, representing the AND of the two inputs (`a & b`).

### Verilog Code:

```verilog
module halfadder(a, b, s, c);
  input a, b;
  output s, c;
  
  assign s = a ^ b;  // Sum: XOR operation
  assign c = a & b;  // Carry: AND operation
endmodule
```

### Functionality

- **Sum (`s`)**: This output represents the sum of the two input bits (`a` and `b`). It uses the XOR (`^`) operation.
  
- **Carry (`c`)**: This output represents the carry of the addition. It uses the AND (`&`) operation.

### Truth Table

| `a` | `b` | `s` (Sum) | `c` (Carry) |
|-----|-----|-----------|-------------|
|  0  |  0  |     0     |      0      |
|  0  |  1  |     1     |      0      |
|  1  |  0  |     1     |      0      |
|  1  |  1  |     0     |      1      |

### How to Use

1. Include this `halfadder` module in your Verilog project.
2. Pass the two input bits (`a` and `b`) to the module.
3. The outputs (`s` for sum and `c` for carry) will be automatically computed based on the inputs.

### Applications

Half adders are used in the design of more complex circuits like full adders and ripple carry adders, which are essential components in building arithmetic logic units (ALUs) for processors.


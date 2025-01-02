# VHDL Counter Overflow Bug

This repository demonstrates a common bug in VHDL code: an integer counter that can overflow without proper handling. The `counter` entity increments a value without checking for the upper limit of the defined range, which can result in unexpected behavior or simulation errors.

## Bug Description
The provided VHDL code implements a simple counter.  However, it lacks a mechanism to prevent the counter from exceeding its defined range (0 to 15).  Once `s_count` reaches 15, the next increment will wrap around to 0 due to the modulo operation implied by the integer range, leading to incorrect counting.

## Bug Solution
The solution introduces a check to prevent the counter from exceeding the upper bound, ensuring that the counter value remains within the specified range.
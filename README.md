# VHDL Counter with Overflow Handling
This repository demonstrates a common error in VHDL counters:  unhandled overflow. The original `counter.vhdl` code increments a counter up to 15 and then wraps around silently. The improved version, `counter_fixed.vhdl`, demonstrates how to handle this situation more gracefully.

## Problem
The original code lacks explicit handling of the counter reaching its maximum value. When the counter reaches 15, it wraps around to 0. Depending on the application this could lead to unexpected behavior or incorrect results.

## Solution
The improved version adds a check for overflow before incrementing the counter. If the counter is at its maximum value, it remains unchanged, preventing unexpected wraparound behavior. This modification makes the counter's behavior more predictable and less prone to errors.
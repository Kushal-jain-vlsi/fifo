# ASYNC. FIFO
This repository contains verilog code for  Async. FIFO
Design of Dual Clock Asynchronous FIFO in Verilog

# Introduction
The Dual Clock Asynchronous FIFO is designed to facilitate data transfer between two different clock domains. It buffers data items from a source clock domain and provides them to a destination clock domain. The FIFO operates asynchronously, handling potential clock domain mismatches.

# FIFO Architecture Overview
The FIFO consists of two primary components: the write side (producer) and the read side (consumer). Each side operates with its respective clock domain and interfaces through the FIFO's memory.

# Memory Organization
The FIFO's memory is organized as an array of storage locations, each capable of storing a data item along with control signals.

# Control Signals
write_clk: Clock signal for the write side (source clock domain).
read_clk: Clock signal for the read side (destination clock domain).
reset: Asynchronous reset signal for the FIFO.
wr_en: Write enable signal from the source clock domain.
rd_en: Read enable signal from the destination clock domain.
empty: Indicates whether the FIFO is empty and has no valid data to read.
full: Indicates whether the FIFO is full and cannot accept any more data.
data_in: Input data from the source clock domain.
data_out: Output data to the destination clock domain.

# Dual Clock Synchronization
Implement clock domain crossing synchronization for control signals using appropriate synchronizer circuits (two-stage or three-stage synchronizers).
Use gray code or other techniques to synchronize the write and read pointers between clock domains.

# FIFO Logic Implementation
Implement storage elements (flip-flops or RAM cells) to store data items in the FIFO's memory.
Use write and read pointers to manage data storage and retrieval.
Implement flow control logic to prevent overflow and underflow conditions.

# Pointer Management
Design the logic for incrementing and wrapping the write and read pointers.
Ensure proper synchronization and glitch-free updates across clock domains.

# Reset and Initialization
Handle asynchronous reset conditions to initialize the FIFO's state properly.
Implement reset logic for control signals and pointers.

# Testing and Verification
Create testbenches to simulate and verify the FIFO's functionality.
Test the FIFO under various scenarios, including empty, full, and transitioning conditions.



Implement metastability handling circuits to address potential synchronization failures at the interface between clock domains.

# Conclusion
The Dual Clock Asynchronous FIFO design is a critical element for enabling data transfer between different clock domains. Careful consideration of synchronization, control logic, and testing is essential to ensure reliable and glitch-free operation.
![png](https://github.com/Kushal-jain-vlsi/fifo/assets/142578632/01251d0d-6c24-4117-b2c6-78f0217bb8fb)


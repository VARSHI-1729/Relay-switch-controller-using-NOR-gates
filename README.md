# Relay-switch-controller-using-NOR-gates
This project was developed during the ChipSphere VLSI Bootcamp to design a digital logic circuit that controls a relay switch based on specific input conditions. The circuit is implemented using only 2-input NOR gates, demonstrating the universal property of NOR gates in digital design.

#What the project does
Logic Design – Derives the minimal Boolean expression for the relay switch operation
Circuit Implementation – Implements the logic using only 2-input NOR gates
Verilog Modeling – Writes behavioral and structural Verilog code for the design
Simulation & Verification – Tests the circuit using a testbench and verifies output waveforms

#Problem Statement
A relay switch is controlled by the output Y of a logic circuit with four inputs A, B, C, D.
The relay must be ON (Y = 1) for the following input combinations:

A	B	C	D
0	0	0	0
0	0	0	1
0	1	0	0
1	0	0	0
1	0	0	1
1	0	1	1
Don't Care Conditions: 0010 and 0110 (these inputs never occur)
For all other input combinations, the relay must be OFF (Y = 0). 
Don't Care Conditions: 0010 and 0110 (these inputs never occur)
For all other input combinations, the relay must be OFF (Y = 0).

Constraint: Design using only 2-input NOR gates.

# Solution Overview
Step 1: Truth Table & K-Map Minimization
The truth table was constructed for all 16 input combinations, incorporating don't-care conditions. Using Karnaugh Map (K-map) minimization, the simplified Boolean expression was derived:  Y = B'C' + AB'

Step 2: NOR-Only Implementation
Using the fact that NOR gates are universal, the expression was transformed to use only NOR gates. The final circuit requires three 2-input NOR gates.

# Language and Tools Used
Verilog – Behavioral and structural modeling

Xilinx ISE – Simulation and waveform analysis

Boolean Algebra – Logic minimization techniques




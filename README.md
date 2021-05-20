# Pipelined-MIPS-Processor-Implementation

# In this project,
you will design a simple 32-bit RISC processor with eight 32-bit 
general purpose registers: R0 through R7. R0 is a normal register, NOT hardwired to zero. The 
program counter PC is a special-purpose 20-bit register. That can address at most 2
20
instructions. All instructions are only 16 bits. There are four instruction formats, R-type, Itype, B-Type and J-type as shown below:

# Phase 1: Building a Single cycle Processor 
It is recommended that you start by building the datapath and control of a single-cycle 
processor and ensure its correctness. You should have sufficient test cases that ensure the 
correct execution of ALL instructions in the instruction set. You should also write test cases 
that show the correct execution of complete programs. To verify the correctness of your 
design, show the values of all registers (R0 to R7) at the top-level of your design. Provide 
output pins for registers R0 through R7, and make their values visible at the top level of your 
design to simplify testing and verification

Phase 2: Building Pipeline processor
Once you have succeeded in building a single-cycle processor and verified its correctness, 
design and implement a pipelined version of your design. Make a copy of your single-cycle 
design, then convert it and implement a pipelined datapath and its control logic. Add pipeline 
registers between stages. Design the control logic to detect data dependencies among 
instructions and implement the forwarding logic. You should handle properly the control 
hazards of the branch and jump instructions. Also, stall the pipeline after a LW instruction, if 
it is followed by a dependent instruction.

# Testing and verification
To demonstrate that your CPU is working, you should do the following:
 Test all components and sub-circuits independently to ensure their correctness. For
example, test the correctness of the ALU, the register file, the control logic separately, 
before putting your components together.
 Test each instruction independently to ensure its correct execution. 
 Write a sequence of instructions to verify the correctness of ALL instructions. Use SET 
and SSET to initialize registers or load their values from memory. Demonstrate the 
correctness of all ALU R-type and I-type instructions. Demonstrate the correctness of LW 
and SW instructions. Similarly, you should demonstrate the correctness of all branch and 
jump instructions
 Test sequences of dependent instructions to ensure the correctness of the forwarding 
logic. Also, test a LW (load word) followed by a dependent instruction to ensure stalling 
the pipeline correctly by one clock cycle. 
 Test the behavior of taken and untaken branch instructions and their effect on stalling the 
pipeline.
 Make several copies and versions of your design before making changes, in case you
need to go back to an older version.

# Test Programs:
1. Write a simple test program that counts the number of 1's in a 32-bit register
2. Write a test program involving procedures and arrays. For example, the main procedure
initializes array elements with some constant values. It then calls a second procedure
after passing the array address and the number of elements as parameters in two 
registers. The second procedure uses the parameters to compute the sum of the array 
elements and returns the result in a register. 
3. Translate each program into machine instructions and load it into the instruction 
memory starting at address 0. You can also save the image of the instruction and data 
memories into files and reload them later for testing purposes.

# Project Report
The report document must contain sections highlighting the following: 
1. Design and Implementation 
 Specify clearly the design giving detailed description of the datapath, its 
components, control, and the implementation details. 
 Provide drawings of the component circuits and the overall datapath. 
 Provide a description of the control logic and the control signals. Provide a table 
giving the control signal values for each instruction. Provide the logic equations 
for each control signal. 
 Provide a description of the forwarding logic, the cases that were handled, and the 
cases that stall the pipeline, and the logic that you have implemented to stall the pipeline
2. Simulation and Testing
 Carry out the simulation of the processor developed using Logisim. 
 Describe the test programs that you used to test your design with enough
comments describing the program, its inputs, and its expected output. List all the 
instructions that were tested and work correctly. List all the instructions that do not 
run properly.
 Describe all the cases that you handled involving dependences between 
instructions, forwarding cases, and cases that stall the pipeline
 Also provide snapshots of the Simulator window with your test program loaded 
and showing the simulation output results.

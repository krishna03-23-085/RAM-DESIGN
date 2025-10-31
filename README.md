# RAM-DESIGN

*COMPANY*: CODTECH IT SOLUTIONS  

*NAME*: KRISHNA SINGH 

*INTERN ID*: CT04DR278  

*DOMAIN*: VLSI 

*DURATION*: 4 WEEKS  

*MENTOR*: NEELA SANTOSH  

##Description 

SYNCHRONOUS RAM DESIGN AND SIMULATION
Objective:

The main objective of this task is to design and simulate a Synchronous Random Access Memory (RAM) using Verilog Hardware Description Language (HDL). The design should allow both read and write operations, controlled by a clock signal, and the correctness of the design should be verified through simulation on an online Verilog platform.

Tools and Platforms Used:

The design and simulation were carried out using EDA Playground — an online cloud-based integrated development environment (IDE) specifically built for HDL coding. It supports Verilog, SystemVerilog, and VHDL languages and allows real-time testing using open-source simulators like Icarus Verilog and Verilator. The tool provides two main sections: one for the design code and another for the testbench, which is used to verify the behavior of the implemented circuit.
The EPWave waveform viewer available on the platform is used to visualize timing diagrams of clock, input, and output signals. This helps in verifying whether the RAM module behaves correctly on every clock edge.

Other than EDA Playground, Verilog HDL serves as the core tool for describing the behavior of the RAM. Verilog is a hardware description language used to model electronic systems at the register-transfer level (RTL). It allows designers to define how digital circuits behave over time using constructs like always blocks, if conditions, and clock sensitivity lists.

Theory and Working:

Random Access Memory (RAM) is a volatile storage device used in digital systems for temporary data storage. A synchronous RAM performs all read and write operations in synchronization with the clock signal. In this task, an 8-bit × 16 RAM is designed — meaning it can store 16 data values, each 8 bits wide, addressed using a 4-bit address bus.

The RAM uses:

Clock (clk): Controls the timing of operations.

Write Enable (we): Determines whether the operation is read (0) or write (1).

Address (addr): Selects which memory location to access.

Data Input (data_in): Carries data to be written.

Data Output (data_out): Outputs data during a read operation.

During simulation, when we = 1, the data at data_in is written into the memory location specified by addr on the rising edge of the clock. When we = 0, the data stored at that address is read out through data_out. The always @(posedge clk) construct ensures that all memory operations happen only when the clock transitions from low to high, ensuring proper synchronization.

Simulation and Results:

The testbench code initializes signals, writes data into a few memory locations, and then reads them back to verify correctness. For instance:

Writing 10101010 to address 0

Writing 11001100 to address 1

Writing 11110000 to address 2

Later, the write enable is disabled, and data is read from these addresses. The EPWave waveform clearly shows that during the write phase, data is correctly stored in memory, and during the read phase, the previously written values are accurately retrieved. This confirms that the RAM module works as intended.

The simulation was executed using Icarus Verilog (v12.0) as the backend compiler and simulator. The timing diagrams displayed expected transitions on each clock cycle — proving successful synchronization between read/write operations and the clock signal.

#Output

<img width="1440" height="855" alt="Image" src="https://github.com/user-attachments/assets/731d72c4-0137-464e-a2fc-86a246cb2b62" />




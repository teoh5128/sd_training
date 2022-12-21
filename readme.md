# SD Training 
Content of training:
- [Day_0 : System/Tool Setup Check. GitHub ID creation](https://github.com/YishenKuma/sd_training/edit/main/readme.md#day_0--systemtool-setup-check-github-id-creation)

> - [Lecture_0](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lecture-topics)
> - [Lab_0](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lab-session)

- [Day_1 : Introduction to iverilog design test bench](https://github.com/YishenKuma/sd_training/blob/main/readme.md#day_1--introduction-to-iverilog-design-test-bench)

> - [Lecture_1 + VSD-IAT recording topics](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lecture--vsd-iat-recordining-topics)
> - [Lab_1](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lab-day_1)

- [Day_2: Timing, Hierarchical vs Flat synthesis, and Efficient flop coding style](https://github.com/YishenKuma/sd_training/blob/main/readme.md#day_2--timing-hierarchical-vs-flat-synthesis-and-efficient-flop-coding-style)

> - [Lecture 2 + VSDIAT recordings](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lecture--vsd-iat-recordining-topics-1)
> - [Lab 2](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lab-day_2)

- [Day_3: Combinational and sequential optimizations](https://github.com/YishenKuma/sd_training/blob/main/readme.md#day_3--combinational-and-sequential-optimizations)

> - [Lecture 3 + VSDIAT recordings](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lecture--vsd-iat-recordining-topics-2)
> - [Lab 3](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lab-day_3)

- [Day_4: GLS/Blocking vs Non blocking Assignments and synthesis simulation mismatch](https://github.com/YishenKuma/sd_training/blob/main/readme.md#day_4-timing-hierarchical-vs-flat-synthesis-and-efficient-flop-coding-style)

> - [Lecture 4+ VSDIAT recordings](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lecture-4--vsd-iat-recordining-topics)
> - [Lab 4](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lab-day_4)

- [Day_5: DFT](https://github.com/YishenKuma/sd_training/blob/main/readme.md#day_5--dft)

- [Day_6: Introduction on logic synthesis](https://github.com/YishenKuma/sd_training/blob/main/readme.md#day_6--introduction-on-logic-synthesis)

> - [Lecture 6 + VSDIAT recordings](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lecture--vsdiat-recording-topics)
> - [Lab 6](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lab-day_6)

- [Day_7: Basic SDC Constraints](https://github.com/YishenKuma/sd_training/blob/main/readme.md#day_7--basic-sdc-constraints)

> - [Lecture 7 + VSDIAT recordings](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lecture--vsdiat-recording-topics-1)
> - [Lab 7](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lab-day-7)
## **Day_0 : System/Tool Setup Check. GitHub ID creation** 

### Lecture Topics

* Chip and Package
<!---
<img src="images/Chip and package.JPG" width="400">
--->
![](https://github.com/YishenKuma/sd_training/blob/main/images/Chip%20and%20package.JPG) 

Chip: The assembly of active and passive electronic components, along with their inetrconnections, fabricated as a single unit on a thin substrate of semiconductor material.

Package: The housing that chips are placed in. The package is then either plugged into or soldered onto the printed circuit board. 

* Wire bonding
<!---
<img src="images/wire_bond.jpg" width="400">
--->
![](https://github.com/YishenKuma/sd_training/blob/main/images/wire_bond.jpg)

Wire bonds are the interconnections between an integrated circuit (IC) or other semiconductor device and its packaging during semiconductor device fabrication.

* Core and IO
<!---
<img src="images/iopads.jpg" width="400">
--->
![](https://github.com/YishenKuma/sd_training/blob/main/images/iopads.jpg)

Core: the section of the chip where the fundamental logic of the design is placed (Macros, IPs, Etc,.)

IO: allows the communication of data between die and external components

IO Pads: acting as gateway, connecting internal signals from the core of the integrated circuit to the external pins of the chip package

* Macros and IPs
<!---
<img src="images/macro IP.jpg" width="400">
--->
![](https://github.com/YishenKuma/sd_training/blob/main/images/macro%20IP.jpg)

Macros: Simple custom built cell serving a sepecific funtional purpose that can be found through open sources

Foundry IPs: Macro cells developed with the intent of licencing to multiple vendor for using as building blocks in different chip designs, known as Intellectual Property 

* Communication between software and hardware
<!---
<img src="images/compilers-assemblers-translators-opener.jpg" width="400">
--->
![](https://github.com/YishenKuma/sd_training/blob/main/images/compilers-assemblers-translators-opener.jpg) 

Compiler: reads the complete source program written in high-level language as a whole in one go and translates it into an equivalent program in assembly language

Assembler: translate the program written in assembly language into machine code represented by binary code

### Lab session

#### Steps

[Setup](https://github.com/YishenKuma/sd_training/blob/main/scripts/github_lab0.txt)

#### Results

<!---
<img src="day0.JPG" width="850">
--->
![](https://github.com/YishenKuma/sd_training/blob/main/day0.JPG) 

> error encountered after source standaloneHome/top.tcl

## **Day_1 : Introduction to iverilog design test bench** 

### Lecture + VSD-IAT recordining Topics 

* RTL

RTL refers to Register Transfer Level, a design abstraction that models a circuit in terms of the flow between signals and the logical operations performed

* Verilog HDL

Verilog Hardware Description Language (HDL) is a language used to describe the behaviour of a circuit.

* RTL Deisgn

The behavioural representation of the required specification, written in verilog HDL

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/11.jpg)

RTL design is checked and verified using simulator for adherence to spec by simulatind the design

* iverilog

iverilog is the tool used for simulating the design, to verify the intent of design

the simulator acts by identifying changes in the input signal and evaluating the output based on changes identified from the input
output file dumped out is known as the vcd (value change format) file, to be viewed in gtkwave tool

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/12.jpg)

* gktkwave

gtkwave is a waveform analyzer tool primarily used for visualization

* Design

Design is the verilog code/codes which has the intended functionality meeting the required specification

* Testbench

testbench applies test vectors to the design to check its functionality

checks wether design is obeying to the required specifications

* Verilog files

design verilog file will need to have an associated testbench_design verilog file to be loaded into iverilog

design and testbench file will have a one to one coorespondance

* Library files

the library file is a collection of modules containinga a variety of standard cells

* Logic synthesis

Synthesizer is the tool used to convert RTL into a netlist

The synthesizer maps the RTL code with the digital logic circuit,using a given library file, to generate a netlist

* Netlist

Design is converted into gates and the connections are made between the gates, this file is given out as the netlist

The netlist can then be verified with the cooresponding testbench through the simulator

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/15.jpg)

* Clock timing and frequency claculation

The library file used in generating a netlist has a different sets of standards cells with variying speeds due to the combinational delay in circuit

Combinational delay in the logic path determines the maximum speed of operatiom of the logic circuit

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/16.jpg)

Because the circuit is affected by setup and hold timings, we need to have a variety usage of cells

* Setup and Hold 

Setup time refers to the time needed for data at input, to become stable before the active edge of clock

Hold time refers to the time needed for data at input, to become stable after the active edge of clock

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/17.jpg)

* Selection of cells

We need cells to work fast to meet the required performance, but will sacrifice power and area
But, to handle hold issues that may be present, we need to have cells that work slow, which will also cause circuit to be sluggish
Guidance is needed for the synthesizer to select the appropriate cells for optimum implementation of the logic circuit, this guidance is offered though the use of constraints 

### Lab Day_1

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/1.jpg)

remote spark ubuntu terminal for coding

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/2.jpg)

cloning github repo in vlsi directory

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/3.jpg)

loading verilog files into simulator, and executing output vcd file for viewing in gtkwave

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/4.jpg)

verilog file used and corresponding testbench file used

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/5.jpg)

loading yoysy softqware to be used for synthesis

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/6.jpg)

reading library and verilog files, then performing synthesis using command "synth -top good_mux"

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/7.jpg)

generating the netlist using command "abc -liberty *lib_path*"

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/8.jpg)

shows graphical representation of realized logic

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/9.jpg)

verilog file written from netlist produced

![](https://github.com/YishenKuma/sd_training/blob/main/day_1/lab/10.jpg)

simplified verilog file written using the -noattr switch 

## **Day_2 : Timing, Hierarchical vs Flat synthesis, and Efficient flop coding style** 
### Lecture + VSD-IAT recordining Topics 
* Fundamental of CMOS

complementary metal-oxide semiconductor 

used for constructing integrated circuit (IC) chips

the outputs of the PMOS and NMOS transistors are complementary to create an inverting output

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/1.jpg)

* Setup and Hold time

Setup Time is the time that the input data signals need to become stable before the active clock edge occurs

Hold Time is the time that the input data signals need to become stable after the active clock edge occurs

* .Lib

Collection of standard cells

The naming of the library includes the specific process (typical/nominal/..), temperature and voltage for the design.

The libraries created are characterized to model the variations in the process, voltage and temperature (PVT)

The variations in the process, temperature and voltage of design determines how the design will operate, and the design should be able to operate across all corners 
with the regard to difference in PVT

The library specifies on needed information for the cell mapping such as the technology, delay model, units of measurements, operating conditions , etc,.

The library holds a variety of cells along specified features of the cells such as leakage power, area, signal used for pins, and features of the cell pins.

Each combination of input that produce a unique output will have a specific leakage power.

Variations of the same types of cells will also have unique features associated.

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/2.jpg)

* Hierachical and Flat Representation

Hierarchical design shows design elements as sub-modules within “top module” rather than seeing the instantiation of gates as in flat synthesis

In a flattened “flat netlist” the hierarchies are flattened, showing all the cells used in the whole design, which is the complete structure, rather than in sub module form

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/3.jpg)

* Sub module synthesis

we perform sub module synthesis when we have multiple instances of same module, or when the design is too complex that it would be better to divide the design into sub modules to be synthesized individually

* Stacked PMOS vs Stacked NMOS

Occasionally library elements may result in the design of a stack PMOS during synthesis

This is undesirable as stacked PMOS due to its poor mobility, therefor during synthesis the logic can be restructured to use other components to create the same logic but under a stacked NMOS

E.g. use of OR gate replaced with NAND gate and INV cells

* Gltches

Glitches are unwanted pulses at the output of combinational gates

These glitches occur due to unbalanced delay to the combinational gates

The glitch at one gate can then be feed into the following component causing the later resulting output net to be extremely glitchy and causing high dynamic power consumption.

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/4.jpg)

* Flops

The presence of flops acts to shield the proceeding elements from being affected by the undesired glitch, as the clock signal is unaffected from data signals and glitches

The clock pin will allow the value to stay stable, and therefor avoid undesired glitches in the proceeding elements

The flops need to be initialized for the combinational circuit to have its desirable output

The flop is initialized through its control pins (Reset | Set)

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/5.jpg)

* Asynchronous vs Synchronous

Asynchronous flops means the output of the circuit will be triggered from the rising edge of the set/reset signal, in addition to the rising edge of the clock signal

Synchronous flops means the output of the circuit will be triggered solely on the rising edge of the clock signal, a rising edge in the set/reset pin will not prompt data to be captured

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/6.jpg)

### Lab Day_2

* Top module synthesis

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/7.jpg)

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/10.jpg)

> Library elements used in sub modules

* flattened module synthesis

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/8.jpg)

* sub module synthsis

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/9.jpg)

* Asynchronous reset flop

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/11.jpg)

> data at q can either change at the rising egde of clock or set signal

> if set pin is toggeled high, the q will turn high as well

> when set pin is low, the q pin will be equal to d pin at the rising edge of clock signal

* Asynchronous set flop

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/12.jpg)

> data at q can either change at the rising egde of clock or set signal

> if set pin is toggeled high, the q will turn high as well

> when set pin is low, the q pin will be equal to d pin at the rising edge of clock signal

* Synchronous flop

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/13.jpg)

> q pin will only changes upon rising clock edge, and not on rising edge of reset pin

> if reset pin is high during active clock edge, then q will be set to 0

* Efficient coding style

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/14.jpg)

> no cells getting mapped during synthesis

![](https://github.com/YishenKuma/sd_training/blob/main/Day_2/15.jpg)

> 3 bit data getting multiplied without addition cells by adding zero bit/bits or with using own data

> multiplying by 2: 111(7) + 0 = 1110(14)

> multiplying by 4: 111(7) + 00 = 11100(28)

> multiplying by 8: 111(7) + 000 = 111000(56)

> multiplying by 9: 111(7) + 00 = 111111(63)

## **Day_3 : Combinational and sequential optimizations** 

### Lecture + VSD-IAT recordining Topics 

* Nature of synthesis and optimization

Synthesis is not a push button solution

It is dependant on the design statement and clarity of implementation

Some areas will have been applied optimization strategies, and some wont

An area or can be flagged for high effort optimization or set to don’t touch status

The more the design is affected by tool methodologies, the more likely it is to divert from the original design intent

* Optimization methodology

The synthesis tool will perform optimization by minimizing cost functions (design rule costs and optimization costs)

Cost functions vary depending on the EDA tool vendor

Optimization of a design will be an iterative process, as the results of synthesis are dependant on multiple factors such as libraries, constraints and coding styles

Optimizations costs = max delay cost + min delay cost + max power cost + max area cost (most important to least important, may vary depending on EDA vendor)

* Boolean Algebra basics

Boolean algebra constitutes a majority of the combinational optimization

![](https://github.com/YishenKuma/sd_training/blob/main/day3/1.jpg)

de morgan rule is used to transfor or gate into inverting nand gate, as or gate uses stacked pmos which is undesirable

![](https://github.com/YishenKuma/sd_training/blob/main/day3/5.jpg)

* Combinational and Sequential Optimization

Constant propagation is the simplification of a combinational circuit through boolean minimization, allowing less components to used Constant propagation occurs for both combinational and sequential logic

Synthesis optimization also allows improvement on circuit delay, as timing constraints may not be met with original logic, thus circuit is optimized by the tool to reduce gate count and minimize delay to value within expectation 

Constant propagation in combinational logic is based on Boolean algebra, whereas for sequential constant propagation, it is dependant on Boolean algebra and timing diagram analysis

![](https://github.com/YishenKuma/sd_training/blob/main/day3/2.jpg)

One of the additional optimization techniques is known as resource sharing, common inputs would be eliminated, which would also increase the number of fanouts, leaving the overall logic to be distorted in comparison to the original logic intent

![](https://github.com/YishenKuma/sd_training/blob/main/day3/6.jpg)

Boundary optimization is another technique used, where the boundaries inside top level design are optimized, the constants are pushed into and out of hierarchy, and rewires feed throughs and complementary signals

![](https://github.com/YishenKuma/sd_training/blob/main/day3/7.jpg)

Register retiming can also be done by readjusting the combinational logic, allowing the overall operating frequency to be increased

![](https://github.com/YishenKuma/sd_training/blob/main/day3/4.jpg)

State optimization is the optimization of unused gates

Cloning is a physical aware optimization that decreases the load of heavily loaded cell by replicating the cell

![](https://github.com/YishenKuma/sd_training/blob/main/day3/3.jpg)

### Lab Day_3

#### Combinational Logic Optimization

![](https://github.com/YishenKuma/sd_training/blob/main/day3/8.jpg)

verilog files used for combinational logic optimizations

![](https://github.com/YishenKuma/sd_training/blob/main/day3/Picture9.jpg)

> evaluating the boolean logic for the first 4 verilog files

opt_check:

![](https://github.com/YishenKuma/sd_training/blob/main/day3/9.jpg)

> based on logic, an and gate is used

opt_check2:

![](https://github.com/YishenKuma/sd_training/blob/main/day3/10.jpg)

> based on logic, an or  gate is used

opt_check3:

![](https://github.com/YishenKuma/sd_training/blob/main/day3/11.jpg)


> based on logic, 3 input and gate is used

opt_check4:

![](https://github.com/YishenKuma/sd_training/blob/main/day3/12.jpg)

> based on logic, and xnor gate is used, and input b is not used for output

multiple_module_opt:

![](https://github.com/YishenKuma/sd_training/blob/main/day3/20.jpg)

> based on logic, input a is fed into submodule 1 with high pin, logic in verilog shows submodule 1 as an and gate

> the output (based on boolean should be a.1=a) will be fed as n1

![](https://github.com/YishenKuma/sd_training/blob/main/day3/23.JPG)

> sub module 2 is removed in design during "synth -top" as output n2 is not initiallised in assigned logic y = c | (b & n1)

> n1 b and c are fed into an and or gate (b and a through and gate, the output and c through or gate)

#### Sequential Logic Optimization

![](https://github.com/YishenKuma/sd_training/blob/main/day3/14.jpg)

dff_const1: 

> while reset pin is high, Q is low

> if reset toggeled to zero, q will not immediately switch to high, but only once triggered by positive edge of clock

![](https://github.com/YishenKuma/sd_training/blob/main/day3/15.jpg)

dff_const2: 

> while set pin is high, Q is high

> since input D is set high, if set is toggeled to low, the value remians high even as triggered by clock, as q = d

![](https://github.com/YishenKuma/sd_training/blob/main/day3/16.jpg)

dff_const3: 

> two flops used where the output of teh first is fed into the second

> output of first flop is similar to dff_const1

> the second flop out put stays high while set is high, once set is low, it will latch to the immdieate value of Q1, but due to delay, the value will be low, until it becomes high at the next positive edge

![](https://github.com/YishenKuma/sd_training/blob/main/day3/17.jpg)

dff_const4: 

> first flop behave similar to dff_const2, where output is high only

> second flop replicates this behaviour as well as its input Q1 is always high, so output q will also be always high

![](https://github.com/YishenKuma/sd_training/blob/main/day3/18.jpg)

dff_const5: 

> output of first flop is similar to dff_const1

> second flop also replicates the behaviour, but since its input is Q1, which toggels from low to high, Q must also toggle from low to high

> reason as to why both flops do not go high at the same time at the first positive clock edge after reset goes low, is because of the delayed capture of data at input, thus value is low until proceeding positive clock edge  

#### Unused Output Optimization

![](https://github.com/YishenKuma/sd_training/blob/main/day3/21.jpg)

Counter_opt:

> for this case, the output is assigned the final bit of count, and the first 2 bits would not have any significance on the output

> whenever count is increased, the final bit is toggeled, and since the output has no dependancies on the first 2 bits, they are unused outputs

> this case is also only using 1 dff, insetad of 3 as supposed when using 3 bit counter, but since there are 2 unused outputs, they are optimized off

> the input of flop will just be the inverted output of the flop

![](https://github.com/YishenKuma/sd_training/blob/main/day3/22.jpg)

Counter_opt2:

> in this case, our output is assigned as 3'b100

> now, we intiallize the design to use all the outputs, thus the 3 bit counter is implemented with 3 flops in the design

> we have a large amount of logic within the design for the use of the adder circuit, since the first 2 bits are used, the logic will be used

> at the output, we have inverted inputs !2!1!0, fed into a nor gate with an inverted C pin, thus the inputs are 2!1!0 ~= 3[3'b100]

## **Day_4: Timing, Hierarchical vs Flat synthesis, and Efficient flop coding style** 
### Lecture 4 & VSD-IAT recordining Topics 
#### Gate level simulation

Running test bench with netlist, instead of the RTL, as Design Under Test

Since netlist is logically same to the RTL code, same test bench will align with the design

Map the appropriate technology parameters from library models at hand, to the synthesized netlist, thus allowing simulation of the netlist

Can be used in dynamic timing analysis as it can take in account various clocks and resets simultaneously, and give insight on the asynchronous performance that STA is not meant for

The reason we run GLS is to verify the correctness of design after synthesis, and ensuring the timing of design is met (GLS run with delay annotation)

![](https://github.com/YishenKuma/sd_training/blob/main/day4/1.jpg)

> https://www.electronicsforu.com/electronics-projects/gate-level-simulation-increasing-trend

#### GLS using iverilog

Design now (netlist not RTL) contains all the standard cells instantiated

Gate level Verilog models now read and given to the tool to produce the vcd file to be viewed in gtkwave

![](https://github.com/YishenKuma/sd_training/blob/main/day4/2.jpg)

#### Netlist vs Gate level verilog models

Gate level Verilog models allow for functional and timing-aware validation

The necessity in performing functional validation is due to the synthesis and simulation mismatches

![](https://github.com/YishenKuma/sd_training/blob/main/day4/3.jpg)

#### Simulation Synthesis Mismatch

* Incomplete or missing sensitivity list:  synthesizer may ignore this, but simulator will adhere to it

example case of missing sensitivity list:

![](https://github.com/YishenKuma/sd_training/blob/main/day4/4.jpg)

Simulator operates based on “activity”, if input does not change, the output will not change

Always block is evaluated only when @sel is changing

But the always block is not sensitive to the changes in i1 or i0, output y not evaluated on changes in i1 or i0, mux acts like a latch

If we want the module to be sensitive to the changes in any signal, the “always @(sel)” statement should be changed to always @(*)

* Complete sensitivity list with mis-ordered assignments (e.g. modelling sequential logic using blocking assignments) 

Example 1 of mismatch due to blocking statement:

![](https://github.com/YishenKuma/sd_training/blob/main/day4/5.jpg)

blocking statements will be executed sequentially

So for left side code, we will have 2 flops, as the values are written such that the value of d remains only at q0 until the next clock cycle

However, for the right side code, q0 is already assigned to d, so the next statement where q is q0,q will be equal to d within same cycle

This problem can be solved by using non-blocking statements, where the order of statements is not important, as the RHS will be evaluated, then LHS updated after time step, there will have to be 2 flops 

* Non standard Verilog coding

* Timing delay (e.g. placing delays on left side of always block assignments, this will not accurately model either RTL or behavioural models)

#### Blocking assignment

![](https://github.com/YishenKuma/sd_training/blob/main/day4/6.jpg)

Can be viewed as a one stop process, statements executed sequentially

The blocking assignment RHS (right-hand side equation) is evaluated, then LHS (left-hand side equation) is updated, without interruption from any other verilog statement 

Blocking assignments blocks trailing assignments in the same always blocks from occurring until after the current assignment has been completed

Temp variable is needed

#### Nonblocking assignment

![](https://github.com/YishenKuma/sd_training/blob/main/day4/7.jpg)

Nonblocking assignments can be viewed as a two step process. At the beginning of the time step, the RHS is evaluated, then at the end of the time step, the LHS is updated.

Non blocking assignments are only made to register data types and are therefore only permitted inside of procedural blocks, such as initial blocks and always blocks

Nonblocking assignments are not permitted in continuous assignments

Nonblocking operator is the same as the less-than-or-equal-to operator (“<=”)

Nonblocking assignment does not block other Verilog statements from being evaluated

#### Stratified event queue

![](https://github.com/YishenKuma/sd_training/blob/main/day4/8.jpg)

Stratified event queue defines how different events are organized into segmented event queues during simulation 

There is no priority for tasks within active event queue, the tasks can be executed in any order

![](https://github.com/YishenKuma/sd_training/blob/main/day4/9.jpg)

#### RTL coding guidelines

Blocking and nonblocking assignments in the same always block should not be mixed

Assignments to the same variable from more than one always block should not be made

Blocking assignments are meant for combinational logics

Nonblocking assignments are meant for sequential logics

Sequential and combinational logics should be kept separate

### Lab Day_4
#### GLS and Synth Sim Mismatch

![](https://github.com/YishenKuma/sd_training/blob/main/day4/10.jpg)

> ternary operator: <Cond>?<T>:<F> , The execution of a parameter assign (e.g. y = x?a:b) is such that, when x is true, y =a, when x is false, y =b 

for this lab simulation, we have a mux selecting between io or i1 based on sel

as can be seen from the waveform, when sel is low, the output is set to i0 waveform

when sel is high, the output is set to i1

![](https://github.com/YishenKuma/sd_training/blob/main/day4/11.jpg)

after performing sysnthesis, we view the gate level simulation, we can see that the behaviour of the output is matching with the previous waveform

thus this case has no synthesis simulation mismatch

![](https://github.com/YishenKuma/sd_training/blob/main/day4/12.jpg)

> bad_mux

now we look at the same file, but the logic is written using an always block, and the always block is set to change whenever parameter sel undergoes change

we can see from the waveform that when sel changes, y is set to the value of i0/i1 at the point of change, but following that, it does not change and remains constant until the next change in sel

this is becuase in our code, we have not initiallized the changing behaviour of i0 and i1 into our design, thus the mux acts as a latch instead

![](https://github.com/YishenKuma/sd_training/blob/main/day4/13.jpg)

now we perform our synthesis and gate-level simulation, and we see from the waveform that now thge output y is also taking into account the changes in i0 and i1, and acts as a mux as intended

this is what is known as the synthesis simulation mismatch

this can be resolved by replacing the "always @ (sel)" statement to "always @ (*)"

 #### Synth Sim Mismatch for blocking statements 
  
![](https://github.com/YishenKuma/sd_training/blob/main/day4/16.jpg)

> blocking_caveat

for this case, the verilog is written using a blockings statement, wherein the output is set to a value of x that is only computed in the proceeding statement, meaning that the final output d is set to previous value of x, causing the output to be delayed by 1 duty cycle

as can be seen from the waveform, the output generated for d is only set in the next cycle

![](https://github.com/YishenKuma/sd_training/blob/main/day4/15.jpg)

now we have perfromed synthesis and we have our gate-level simulation

looking at the output data d, we can see that the output is not being delayed anymore, and the correct data is being displayed on the same duty cycle

there difference in the simulation clearly shows the synthesis simulation mismatch due to the use of the blocking statement

this can be solved by rearranging the order of the statements, or by using nonblocking statements

## **Day_5 : DFT** 

#### Testability

Layman terms: “A characteristic of an item’s design which allows the status (operable, inoperable, degraded) of that item to be confidently and quickly determined”

VLSI terms: “If a design is well controllable and well observable, it is said to be easily testable”

### The 3 Ws for DFT _ What, Why , Where/When

#### What:

DFT is a technique used to facilitate a design to become testable after production, or, the technique of adding an extra design to make sure it is tested after fabrication

Some examples of designs for making chips testable:

* for macros, MBist, Memory Built in self test, logic are used
* For flops, scan chains are used
* For combinational circuits, test patterns are generated, the number of test patterns will be based on the number of inputs (patterns = 2^inputs)

#### Why:

It makes testing easy at the post-production process

Chips can be tested through 3 levels after fabrication:

* Chip level, when chip is fabricated
* Board level, when chip is integrated on board or package
* System level, when several boards are assembled together

DFT is also done due to the economical and market needs, performing testing at the early stages such as chip level finding a defect in the manufacturing can prevent great loss if the fault is detected at user end, where the risk is much too high to allow, it is best to find the errors at chip level to avoid unnecessary losses

#### Where/When:

When? DFT is inserted at the beginning of design flow

Where? DFT is inserted during synthesis stage, the DFT code should be a synthesizable before being manufactured, thus it needs to be inserted during synthesis

![](https://github.com/YishenKuma/sd_training/blob/main/day5/1.jpg)

>  Asic design flow

### Pro’s and Con’s

#### Pros

* Reduces tester complexity
* Reduces tester time (70% of production of chip is due to testing time)
* Reduces chance of loss due to faulty device going to user end

#### Cons

* Adds complexity to design flow
* Increases power, area, and package pins (due to additional circuitry and pins)
* Design time will increase

### Basic Terminologies

#### Controllability

From DFT point of view, both ‘0’ and ‘1’ need to be able to propagate to each and every node within target patterns

A point is said to be controllable if both ‘0’ and ‘1’ are propagated through the scan patterns.

![](https://github.com/YishenKuma/sd_training/blob/main/day5/2.jpg)

> through the introduction of the mux for each register, we can check though the registers to see which might be faulty and causing the final output to be incorrect, insteas of testing each node one by one, this allows you better control of the design

#### Observability

To make sure each node is controllable, we need to have observability

Observability is the ability to measure the state of a logic signal

To measure a node means that the value at the node can be shifted out through scan patterns and can be observed through scan out ports

![](https://github.com/YishenKuma/sd_training/blob/main/day5/3.jpg)

> Through the usage of flip-flops, which allows the data to be observed at the output of the flops without affecting the design 

#### Fault

A physical damage/defect (fabrication defects) compared to the good system, which may or may not cause system failure

#### Error

The result of a fault, where system goes into erroneous state

#### Failure

System not providing expected service

A fault causes error which leads to system failure

#### Fault coverage

Percentage of the total number of logical faults that can be tested using a given test set T

There will be a list of checks to be made from the tests, ensuring no error is happening, the number of tests completed that are false over the total number of tests is what is known as the fault coverage

#### Defect Level

Defect level is the fraction of shipped parts that are defective, or the proportion of the faulty chip where fault is not detected and was classified to be good

### DFT Techniques

#### Ad-hoc technique

This technique needs to be done in the initial designing stages, or else it will lead to problems in the post-production stages when testing

Steps:

* Avoid combinational feedback

Raise-around condition, refers to when the output of a combinational block is feedback to its input, the signal at the input cannot be determined between the old value or the new feedback value

To mitigate that, we simply add a 1-bit register which acts as a flip flop, connected to a clokc, to ensure there will be no raise at the feedback input pin

* All flip flops must be initialized

There are cases where flip flops may go into a high impedance x-unknown state, where the output value is an unknown value x. how we can exit from this state is by resetting the flip-flops, so the set/reset pins need to be usable for the flip-flops

* Partition a large circuit into smaller blocks

Breaking large design into smaller partitions so that it can be easier to solve

* Provide test control for the signals which are not controllable

Need to add the circuitry needed to nodes to allow for the observability and controllability 

* the ATE requirements have to be considered while designing the test logic

ATE (Automatic Test Equipment) or ATGP (Automatic Test Pattern Generator) is what is used in the case where a high number of flops is used and the number of test patterns increase to a value we cannot put up manually

ATE Functionality: Scan-in phase, Parallel Measure, Parallel capture, First Scan-Out Phase, Scan-out phase

#### Structured technique 

There are a few limitations present in the ad-hoc technique, thus the structured technique was developed to improve on these limitations

* Scan

All the flip-flops are converted to scan flip-flops

* Boundary scan

Similar to scan but limited to boundary, essentially breaking the design into smaller partitions and working through them

* Built-in self-test

MBist (Memory built in self-test): Instead of designing another testable circuit for macros from scratch, the company providing the macro has already provides a built in self-test in the memory. For a macro, all the conditions will be stored in a memory, we will need to run the built in self-test to see the expected outputs based on the inputs we give. All the corner cases will be tested.

LBist (logic built in self-test): checks gates based on the logic that the component should operate on 

### Introduction to scan-chains

#### scan-chain technique

* specifying the scan constraints
* specifying scan ports and scan enables
* compiling the dft
* identifying the number of scan chains

#### scan based technique

Scan chains are elements in a scan-based design that is used to shift-in and shift-out the test data

As mentioned previously, the addition of the 1-bit register allow for observability, however we cannot have a register added to every node of logic in the design, as that would increase area used immensely

Instead, the more optimum method is to use a scan-chain, where a chain is formed by a number of flops connected back to back in a chain, with the output of one flop being connected to another

The input of the first flop is connected to the input pin of the chip (called scan-in) from where the scan data is fed. the output of the last flop is connected to the output pin of the chip (called scan-out) which is used to take the shifted data out

 Scan enable is like an enable line for the scan elements

The scan in is done using an additional mux

There are 3 types of scan lfip-flops configurations: multiplexed, clock,lssd

![](https://github.com/YishenKuma/sd_training/blob/main/day5/4.jpg)

> conversion of normal d flip-flop into muxed flip-flop, which is a scannable flip-flop

The longer the length of a scan chain, the higher the number of cycles required to shift the data in and out. 

A smaller scan chain length with same number of flops, would mean that the number of input/output ports needed as scan_in and scan_out ports are increased.

The length of the largest scan chain is determined by the number of cycles required to run a pattern. The number of ports required is twice the number of scan chains. 

The length of a scan chain can be determined through the correlation of clock cycles required during Scan In and Scan Out operations. The number of cycles required for a ATPG pattern determines th number of flip flop in the longest scan chain, thus the length of the scan chain.

#### purpose of scan flops

Main 2 reasons are:

* test the stuck-at faults in the manufactured devices, ensure that the faults can be controlled through the muxes
* test the paths in the manufactured devices for delay, to test whether each path is working at functional frequency or not.

#### Functionality of scan_chain

Goal of scan chain: to make each node in the circuit controllable and observable

Steps to perform basic scan-in and scan-out:

1. assert scan_enable (make it high) so we enable (SI -> Q) path for each flip-flop
2. keep shifting in the scan data until the intended values at the intended nodes are reached
3. de-assert_scan_enable (make it low for one pulse of clock, in case of stuck-at-testing and two or more cycles in case of transition testing), to enable the D -> Q path, so that the combinational cloud output can be captured at the next clock edge. The capture data is propagated through each register/flip-flop at every clock egde.
4. assert scan_enable once again and shift out the data through scan_out

![](https://github.com/YishenKuma/sd_training/blob/main/day5/5.jpg)

> https://anysilicon.com/overview-and-dynamics-of-scan-testing/

![](https://github.com/YishenKuma/sd_training/blob/main/day5/6.jpg)

> scan port is put in serially trough the from scan in port
> at the first clock edge, the data will be shifted in to the flip-flop, for each following data, the data will be shifted in at each clock edge. 

![](https://github.com/YishenKuma/sd_training/blob/main/day5/7.jpg)

> Capture is run at a slower frequency to detect Stuck-At faults
> Before arrival of next active clock edge, the test pattern response is processed by the combinational logic and becomes available at the D input of next flip-flop
> As soon as the active clock edge arrives, the processed test pattern response is captured by the next flip-flop and becomes available at the Q pin.

![](https://github.com/YishenKuma/sd_training/blob/main/day5/8.jpg)

> once capture is complete, the response test pattern is shifted out 
> we compare the data after it has been completely propagated to its functional data by de_asserting the scan enable, meaning the functional data is passed through
> if there is no mismatch between the output scan data and the functional data, then the combinational circuit outputs of the design are good, ensuring the registers and wires are not faulty

![](https://github.com/YishenKuma/sd_training/blob/main/day5/13.jpg) 

#### Overview of DFT compiler

![](https://github.com/YishenKuma/sd_training/blob/main/day5/14.jpg)

> DRC checks are performed before and after scan to ensure that the design rules are being violated due to the scan insertion

![](https://github.com/YishenKuma/sd_training/blob/main/day5/15.jpg)

> where synopsys-DFT comes into play

## **Day_6 : Introduction on logic synthesis**

### Lecture + VSDIAT recording topics

##### takeaway from RTL course

Digital logic is a very powerful switching function used in automation and decision making

As digital logic has such a good role in performing decision making, it has become the basis for computing, electronic devices and control systems in our advancing digital world.

These specifications / behavioural models are written in HDL (Hardware Description Languages) such as VHDL or Verilog

These specifications are then represented in a programming language, which is RTL (Register Transfer Logic)

#### what is logic synthesis

In order to get the physical digital circuit that we want, we must perform synthesis, where the design is converted into gates and the connections are made between the gates, the given output file is the netlist.

This process is also known as RTL to Gate Level Translation

![](https://github.com/YishenKuma/sd_training/blob/main/day6/1.jpg)

The RTL files is used along with a .lib file to generate the netlist though synthesis

* .lib and implementation

The collection of logical modules with varying performance specifications

The .lib file consists of various flavours of gates to allow for use of gate at different operating speed, to accommodate for timing conscious circuitry (Setup and hold timings)

Faster cells allow for lesser cell delay, but the drawback is increased power and area, whereas slow cells require less power and area, but add more delay to the path

The guidance in order for synthesizer to select the appropriate cells to be used at paths is done through the constraints given

![](https://github.com/YishenKuma/sd_training/blob/main/day6/2.jpg)

The synthesized circuit can have different implementation, as the boolean logic can be restructured in various ways, meaning the synthesized circuit will have different sets of cells used, meaning the delay and paths would be different. 

The synthesis will need to produce the most beneficial implementation dependent  on the sconstraints set for the given design

The working digital logic circuit must be logically correct, electrically correct and timing met

#### Intro to DC

Design Compiler (DC) is a tool used for synthesis targeted for ASIC design flow from synopsys

Features include:

* It is a premium synthesis tool used across semiconductor industry

* Design compiler has interperability with various backend tools from synopsys, meaning it gels well with other synopsys backend tools

* Able to perform DFT scan stitch

* Can handle huge designs with extreme complexity and provide good QoR, Quality of Results

#### Terminologies associated with DC

* SDC

Synopsys Design Constraints

These industry standard design constraints are supplied to DC to guide the tool for appropriate and suitable optimization to achieving best implementation

It is used across EDA (Electronic Design Automation) implementation tools which are provided by different tool vendors

Specifies design intent in terms of the timing, power and area constraints

SDC is based on Tool Command Language, TCL

* .lib

Design library containing the standard cells

* DB

Similar to .lib, but using a different format, as DC understands libraries only in .db format. 

.lib must be converted into .db 

* DDC

Synopsys proprietary format for storing the design information

DC can write out and read in DDC

DDC has all the information loaded in the tool memory

* Design

The RTL file which has the behavioural model of the design

#### DC Setup

![](https://github.com/YishenKuma/sd_training/blob/main/day6/3.jpg)

#### Implementation Flow of ASIC

The steps in converting RTL to the Physical Database, GDS format

![](https://github.com/YishenKuma/sd_training/blob/main/day6/4.jpg)

#### DC Synthesis Flow

![](https://github.com/YishenKuma/sd_training/blob/main/day6/5.jpg)

#### TCL basics

TCL is the language used for writing the sdc files

All the dc internal commands are based on TCL only 

* set

Create and store information in variables

Square brackets are used for nesting the commands in TCL

![](https://github.com/YishenKuma/sd_training/blob/main/day6/6.jpg)

The variables can be shown using echo $"variable"

The "$variable" cannot be used during set, it must be set variable

* if {condition} {statement} else {statement_2}

Executes statement only if condition is true, else executes statement_2

![](https://github.com/YishenKuma/sd_training/blob/main/day6/7.jpg)

* while {condition} {statement}

Enters a repetitive loop to executing statement as long as the condition is met

![](https://github.com/YishenKuma/sd_training/blob/main/day6/8.jpg)

Incorrect writing of the while loop can lead to infinite loop, as condition may be written in such a way that the condition is always true

![](https://github.com/YishenKuma/sd_training/blob/main/day6/9.jpg)

* for {looping var} {condition} {looping var modification} {statement}

Executes a statement if condition is met based on the looping variable set , and executes until the condition is no longer met due to the looping var modifications in each iteration of loop

![](https://github.com/YishenKuma/sd_training/blob/main/day6/10.jpg)

* foreach var list {statements}

Executes command for every element present in the variable list

![](https://github.com/YishenKuma/sd_training/blob/main/day6/11.jpg)

* foreach_in_collection var collection {statements}

Specific to synopsys tools

Excecutes command for each element in the collection , similar to list, but returned by many dc commands

![](https://github.com/YishenKuma/sd_training/blob/main/day6/12.jpg)

### Lab Day_6
#### Invoking DC basic setup

![](https://github.com/YishenKuma/sd_training/blob/main/day6/13.jpg)
 
> Cloning github files into unix environment

![](https://github.com/YishenKuma/sd_training/blob/main/day6/14.jpg)

> loading dc_shell

![](https://github.com/YishenKuma/sd_training/blob/main/day6/15.jpg)

> The tool points to your_library.db library file, which is an imaginary non-existent library file, a dummy library pointed to in dc

![](https://github.com/YishenKuma/sd_training/blob/main/day6/16.jpg)

> verilog file used for synthesis

![](https://github.com/YishenKuma/sd_training/blob/main/day6/17.jpg)

> Theoretical logic representation of verilog file 

![](https://github.com/YishenKuma/sd_training/blob/main/day6/18.jpg)

> reading the library file

Dc will load internal dbs in the dc memory to infer the design first

The tool will try to understand the design using gtech

It invokes HDL compiler as the codes used are written in verilog

The warning given, cant read link_library is because the dummy variable is not set to any real variable, we must initialize the variable appropriately

Once the source file is compiled the registers are inferred

The register inferred is a I bit flip flop with AR (asynchronous reset)

![](https://github.com/YishenKuma/sd_training/blob/main/day6/19.JPG)

> written netlist not linked with sky123 lib, but instead using virtual libraries

Internal virtual libraries have been inferred in the netlist after the input and output have been declared

These libraries are known as GTECH, they are used since no proper library path was declared for the design
 
![](https://github.com/YishenKuma/sd_training/blob/main/day6/20.jpg)

> GTECH is still being used instead of the sky libs, the reason for this is because the 2 variables $link_library and $target_library has not been set

![](https://github.com/YishenKuma/sd_training/blob/main/day6/21.jpg)

> The star signifies the libraries that are already in DC memories, as we do not want to override them, we do not want to lose any libraries that may be used by the tool

![](https://github.com/YishenKuma/sd_training/blob/main/day6/22.jpg)

> Now the tool can link the sky lib for performing synthesis

![](https://github.com/YishenKuma/sd_training/blob/main/day6/23.JPG)

> Running compile command

![](https://github.com/YishenKuma/sd_training/blob/main/day6/24.JPG)

> Now we can see that the netlist is no longer using GTECH and is using the components from the sky130 lib file

#### ddc gui with design_vision

![](https://github.com/YishenKuma/sd_training/blob/main/day6/25.JPG)

> A ddc file must be written out to be viewed by the design_vision tool

![](https://github.com/YishenKuma/sd_training/blob/main/day6/26.JPG)

> Exit and use command "design_vision" to invoke tool to view design

![](https://github.com/YishenKuma/sd_training/blob/main/day6/27.JPG)

> Read the ddc file in the design_vision tool

![](https://github.com/YishenKuma/sd_training/blob/main/day6/28.JPG)

> We cannot read the verilog file written "lab1_flop_net_3.v", the library path will be set to the GTECH paths, as this command will only read the verilog file 

![](https://github.com/YishenKuma/sd_training/blob/main/day6/29.JPG)
 
> Reading the ddc file allows the library paths to be included into the tool when read, as the ddc file saves all information in the tool memory during the used session

![](https://github.com/YishenKuma/sd_training/blob/main/day6/30.JPG)

> The advantage of using the ddc file is that ddc is Synopsys propriety format, meaning that it can only be read by synopsys tools, so we can write the ddc file from DC and hen read it in ICC tool

![](https://github.com/YishenKuma/sd_training/blob/main/day6/31.JPG)

> Viewing the schematic of the design, double clicking the module allows to view all the standard cells present

![](https://github.com/YishenKuma/sd_training/blob/main/day6/32.JPG)

> Schematic is matching with the verilog file read, only difference to note is the inverter connected to the reset pin, however, this is due to the flop reset pin being active low

#### dc synopsys dc setup

Every time we open DC, the 2 variables need to be set

set target_library DC_WORKSHOP/lib/sky130_fd_sc_hd__tt_025C_1v80.db

set link_library {* $target_library}

This is a very tiresome and error prone disadvantage with using this process

The solution to this is though the use of .synopsys_dc.setup 

There will be 2 versions of this file, one in the DC installation area, and one in the DC home area

One advantage that DC flexibility offers is that DC will pick the .synopsys_dc.setup file if it is present in the home directory before looking to the installation directory, so we can make changes to the file in the home directory to perform the repetitive tasks for tool setup, meaning we will not have to manually set the target_library and link_library each time dc is invoked

![](https://github.com/YishenKuma/sd_training/blob/main/day6/33.JPG)

> Writing a .synopsys_dc.setup file to be used by dc during invocation

![](https://github.com/YishenKuma/sd_training/blob/main/day6/34.JPG)

> Now we can see that the target_library and link library have already been set because it was read from the .synopsys_dc.setup file

![](https://github.com/YishenKuma/sd_training/blob/main/day6/35.JPG)

> If we alter the file naming even slightly, it may not be picked up by the tool

![](https://github.com/YishenKuma/sd_training/blob/main/day6/36.JPG)

> Now that the naming is not correct, the commands are not read and thus dc tool library path will once again be set to their imaginary paths

#### tcl scripting

![](https://github.com/YishenKuma/sd_training/blob/main/day6/37.JPG)

> Usage of set and for loop commands

![](https://github.com/YishenKuma/sd_training/blob/main/day6/38.JPG)

> Performing arithmetic using expr to perform calculation on variable

![](https://github.com/YishenKuma/sd_training/blob/main/day6/39.JPG)

> Usage of while loop

![](https://github.com/YishenKuma/sd_training/blob/main/day6/40.JPG)

> Usage of foreach loop

![](https://github.com/YishenKuma/sd_training/blob/main/day6/41.JPG)

> Difference to note between list and collection is that elements in a collection will be printed within brackets {}, a collection is a synopsys propriety format

![](https://github.com/YishenKuma/sd_training/blob/main/day6/42.JPG)

> Usage of foreach_in_collection 
 
## **Day_7 : Basic SDC Constraints**

### Lecture + VSDIAT recording topics

#### Intro to STA

##### Max and Min delay Constraints

![](https://github.com/YishenKuma/sd_training/blob/main/day7/1.jpg)
 
The max frequency that this path can operate on can be used to set the constraint the max delay that the combinational circuit must be. The signal launched from DFFA on clock edge should reach DFFB setup time before next clock edge.

The maximum time the combinational circuit takes including setup time of flop b must be less than the time period of clock received by both flops.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/2.jpg)

The min delay constraint is just as important as having the max delay constraint. For circuit to work properly, the signal launched by DFFA on clock edge should reach DFFB only after hold time has passed after the clock edge.  

The minimum delay of combinational circuit must be greater than the hold time of DFFB , as the data should not change within the hold window.

##### Delay

![](https://github.com/YishenKuma/sd_training/blob/main/day7/3.jpg)

We can use the water bucket analogy to explain the importance of delay. The aim is to fill the bucket with water.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/4.jpg)

The time taken is determined by the inflow, the lower the inflow, the higher the time needed.

In digital logics, the time for the gate to go from 0 to 1 is determined by the delay, the lower the inflow, the higher the delay. In terms of digital logics, the inflow of water is equivalent to the inflow of current, or the input transition, the lower the input transition, the higher the delay in circuit.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/5.jpg)

Now we look at the analogy with the same inflow for both cases, but the size of the bucket is larger for case 1

![](https://github.com/YishenKuma/sd_training/blob/main/day7/6.jpg)

The larger the size of bucket, the longer the time taken to fill bucket. In terms of digital logic, delay is a function of load capacitance, the higher the load capacitance, the higher the delay.

High delay can come from either low input transition into gate, lengthy nets, or nets with high fanouts. Delay of cell will be a function of input transition and output load. We can attempt to reduce delays caused by these issues by either upsizing cell to increase input transition, or shorten the length of route between elements, or inserting buffers in between to reduce the load.

##### Timing ARC

* Combinational Cell

The delay information from every input pin to every output pin which it can control is present in the timing arc

![](https://github.com/YishenKuma/sd_training/blob/main/day7/7.jpg)

In the case of this mux, the output y is dependant on the 3 input pins i0, i1 and y, thus there will be 3 timing arcs, as the change in any of the input pins can cause a change in the output pin

* Sequential Cell

![](https://github.com/YishenKuma/sd_training/blob/main/day7/8.jpg)

For flip-flops, the delay information from clock to Q will be present in the timing arc, as the output can only change based on the change in clock

For latch, the delay from clock to Q, and the delay form D to Q will be present in the timing arc, as the output may change based on change in either clock or D

We also have setup and hold time requirements

![](https://github.com/YishenKuma/sd_training/blob/main/day7/9.jpg)

1 matter to note is that the setup and hold does not occur from pos level clk for PosLevelDlat, and neg level clk for NegLevelDlat. Setup hold is around the sampling point of the clock. There is a distinct difference in the sampling point for pos/neg edge DFF and Pos/Neg level Dlat. The sampling edge will occur at the point before data becomes opaque while still transparent.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/10.jpg)

##### Timing Paths

![](https://github.com/YishenKuma/sd_training/blob/main/day7/11.jpg)

The timing path is the path between the start point and end point, where start point is the input port or clock pin of sequential element, and end point is the output port or D pin of sequential element

![](https://github.com/YishenKuma/sd_training/blob/main/day7/12.jpg)

In this example, we are having 2 timing paths with delay of 1.7ns and 1.2ns respectively.

Based on the previous discussion, we can derive an equation for max delay Tck, which is,

Tck => Tcq + Tcomb +Tsetup

TckA => 0.5 +1.2 + 0.5 => 2.2ns [Critical Path]

TckB => 0.5 + 0.7 +0.5 => 1.7ns

TckA is having a higher value of max delay, thus it becomes our critical path, and our frequency will be defined on this value

Fclk = ½.2ns = 454.5Mhz

We can achieve a better frequency in this circuit by improving the delay on the critical path, the way we can do this is by setting constraints on the elements to limit the value of delay

#### Constraints

In setting constraints for the design, we must first establish how much delay is acceptable.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/13.jpg)

In practice, we have a desired frequency for the circuit to operate on, thus we need to calculate the acceptable delay based on this. We must squeeze the combinational logic delay such that the desired frequency is achievable.

Once the clock period is defined, the synthesis will work to optimize the logic based on the clock period, and the delays between the reg to reg paths will be limited, and the appropriate cells will be selected form the libs to meet the delay needed.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/14.jpg)

Now if we look from a bigger picture, we are having more reg to reg paths as the number of elements begin to become more complex outside a boundary. These are synchronous paths, and thus the input and outputs needs to be constrained as well to squeeze the delay.  

* Reg to Reg is constrained by clock ( Tck => Tcq + Tcomb + T su)

* Reg to Out is constrained by Output external delay and clock period

* In to Reg is constrained by Input external delay and clock period

The Reg to Out and In to Reg are called IO paths and the delay modelling referred is called IO delay modelling. IO delay modelling is usually based on STD interface specifications

we must set the constraint on the external delay because we are having 2 unknown delays from the internal combinational logic and the external, thus we can split the available time between the 2 through constraining the external delay

In handling constraints, we must be aware of the budget of the design for external module, and collect all the necessary information in planning the synthesis, so that we can understand properly and create good constraints.

#### INP Trans Output Load

If we look at our case at an idealistic perspective, the IO Delay modelling should be sufficient for setting the delays to allow for desired frequency

![]( https://github.com/YishenKuma/sd_training/blob/main/day7/15.jpg)

However, our signals are not always ideal, as signals do not have zero rise time, thus input transition is playing a role in creating delay that was not accounted, thus we must model our input transition delay as well, which will further squeeze the logic so that the timing is met

![](https://github.com/YishenKuma/sd_training/blob/main/day7/16.jpg)
 
The next thing we need to consider is the output load, as the cell delay affected by it, and if we do not take into and model the load, then the output logic will behave differently, as this is a parasitic net, not an ideal net. Thus, the logic needs to be squeezed further again to factor in the output load. General rule is to set 70% of timing for external delay and 30% for internal delay.

The value that needs to be modelled for the input transition and output load is determined by the spec. if in the case that the external input and outputs are interfaces at the chip boundary, then the interfaces would have specifications that can determine value of load 

If we have 2 models that are synthesized separately, we can perform the budgeting by discussing with the module owners to set the appropriate constraints

We need to have an optimum budgeting for setting the constraints, as under-budgeting causing setup violations, and over-budgeting may lead undesired effects such as high leakage power and high area consumption

#### Timing dot Libs

We have mentioned previously that the .db is what is used by the tool for reading the lib for the design. We cannot read the .db, however we are able to read the .lib file to understand the information present and how the tool infers the information.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/17.jpg)

Aside from the information discussed preciously that can be found in the .lib such as PVT settings and unit for current, power, voltage ,.etc, we can also find the max transition and max capacitance.

Max transition refers to the maximum slew that is allowed at the input pin of cell.

Max capacitance refers the maximum allowed capacitance on the output pin of a cell.

These 2 are used as a last line of defence to model the design in such a way to control the capacitances and transition times. For example, for high fanout out nets that would accumulate high capacitance, the tool will perform buffering on the nets so that the capacitance at the output pin does not violate the max capacitance set. Users are able to manually set the values for max capacitance and max transitions to constrain the design.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/18.jpg)

As mentioned before, delay is a function of input transition and output load

![](https://github.com/YishenKuma/sd_training/blob/main/day7/19.jpg)

The library provides a table for every cell specifying the input trans and output load and the resulting delay. The tool will be able to know the input trans and output load for each device imported from libs based on the lookup table. 

![](https://github.com/YishenKuma/sd_training/blob/main/day7/20.jpg)

However, the lookup table cannot specify all the values that me be used, thus there may be interpolation done for the values in between data in lookup table to acquire an accurate value.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/21.jpg)

The lookup table is not limited to delay, it can be used for getting data for multiple other specifications in the lib.

Each cell will be having varying flavours meaning different drive strength, cell area, leakage power, pin capacitance, max allowed transition per pin. Functionality and assignment of pins are also shown in the ./lib, known as attributes The data in the .lib is also specified for power and timing factors separately. The tool understands the connections and assignments of cells through the attributes specified in the lib.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/22.jpg)

Unateness refers to the behaviour of cell as a rising input is fed through. Positive unate is when the rising input results in a rising output or no change in output. Negative unate is when the output is the inverted version of input logic. Non-unate refers to when the positive unateness and negative unateness is seen from a cell.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/23.jpg)

Unateness is important as the tool uses the information to propagate the transition.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/24.jpg)

For sequential cells, the timing sense can differ based on the rising or falling edge, as Q may be rising or falling with respect to clock.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/25.jpg)

The setup timing for posedge and negedge flops will be known by the tool from the data that is given from the lib file, as this information is present as written for the specific timing type

![](https://github.com/YishenKuma/sd_training/blob/main/day7/26.jpg)

The related pin also shows the appropriate edge that the timing type should be, as “_N” refers to the inverted state of pin, thus as can be seen above, the timing type for CLK_N is setup_falling while for CLK it is Setup_rising.

![](https://github.com/YishenKuma/sd_training/blob/main/day7/27.jpg)

For latches, as we mentioned before, the pos latch will sample the data on negative edge before opaque state, whereas for Neg latch, data will be sampled on the rising edge

![](https://github.com/YishenKuma/sd_training/blob/main/day7/28.jpg)

The tool can get this data from the lib file as well.

This info present in the .lib tells the tool what to do for setup calculation during specific egdes.

### Lab day 7

#### Querying the properties of .lib from dc shell

* list_lib 

![](https://github.com/YishenKuma/sd_training/blob/main/day7/29.jpg)

> shows the libraries that have already been loaded

* get_lib_cells

![](https://github.com/YishenKuma/sd_training/blob/main/day7/30.jpg)

> query all the and gates in the library

* sizeof_collection

![](https://github.com/YishenKuma/sd_training/blob/main/day7/31.jpg)

> displays number of collection queried

* foreach_in_collection

![](https://github.com/YishenKuma/sd_training/blob/main/day7/32.jpg)

* get_lib_pins

![](https://github.com/YishenKuma/sd_training/blob/main/day7/33.jpg)

* get_attribute

![](https://github.com/YishenKuma/sd_training/blob/main/day7/34.jpg)

> foreach_in_collection x [get_lib_pins sky130_fd_sc_hd__tt_025C_1v80/sky130_fd_sc_hd__nand4b_4/*] {echo [get_object_name [get_lib_pins $x]] "="  [get_attribute [get_lib_pins $x] direction]} 

> command prints pin names with associated direction

* get_lib_attribute

![](https://github.com/YishenKuma/sd_training/blob/main/day7/35.jpg)

> foreach_in_collection x [get_lib_pins sky130_fd_sc_hd__tt_025C_1v80/sky130_fd_sc_hd__nand4b_4/*] {echo [get_object_name [get_lib_pins $x]] "="  [get_lib_attribute [get_object_name [get_lib_pins $x]] direction]}

> command prints pin names with lib associated direction

![](https://github.com/YishenKuma/sd_training/blob/main/day7/36.jpg)

> foreach_in_collection x [get_lib_pins sky130_fd_sc_hd__tt_025C_1v80/sky130_fd_sc_hd__nand4b_4/*] {echo [get_object_name [get_lib_pins $x]] "="  [get_lib_attribute [get_object_name [get_lib_pins $x]] function]}

> command prints pin names with lib associated function

> 4 input nand gate should show !A|!B|!C|!D , in our run the !A is replaced with A_N meaning inverted pin

* script to filter pins by output pins and show function

![](https://github.com/YishenKuma/sd_training/blob/main/day7/37.jpg)

![](https://github.com/YishenKuma/sd_training/blob/main/day7/38.jpg)

* get_lib_attribute $cell area

![](https://github.com/YishenKuma/sd_training/blob/main/day7/39.jpg)

* get_lib_attribute $input_pin capacitance

![](https://github.com/YishenKuma/sd_training/blob/main/day7/40.jpg)

* get_lib_attribute $input_pin clock

![](https://github.com/YishenKuma/sd_training/blob/main/day7/41.jpg)

![](https://github.com/YishenKuma/sd_training/blob/main/day7/42.jpg)

* get_cells -filter

![](https://github.com/YishenKuma/sd_training/blob/main/day7/43.jpg)

* list_attributes

![](https://github.com/YishenKuma/sd_training/blob/main/day7/44.jpg)



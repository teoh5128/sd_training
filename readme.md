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



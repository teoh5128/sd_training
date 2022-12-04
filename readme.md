# SD Training 
Content of training:
- [Day_0 : System/Tool Setup Check. GitHub ID creation](https://github.com/YishenKuma/sd_training/edit/main/readme.md#day_0--systemtool-setup-check-github-id-creation)

> - [Lecture_0](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lecture-topics)
> - [Lab_0](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lab-session)

- [Day_1 : Introduction to iverilog design test bench](https://github.com/YishenKuma/sd_training/blob/main/readme.md#day_1--introduction-to-iverilog-design-test-bench)

> - [Lecture_1 + VSD-IAT recording topics](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lecture--vsd-iat-recordining-topics))
> - [Lab_1](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lab-day_1)

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
* HDL
* RTL Deisgn
* Logic synthesis
* iverilog
* gktkwave
* Design
* Testbench
* Netlist
* Verilog files
* Library files
* Clock timing and frequency claculation
* Setup and Hold 
* Selection of cells

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

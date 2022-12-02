# SD Training 
Content of training:
- [Day_0 : System/Tool Setup Check. GitHub ID creation](https://github.com/YishenKuma/sd_training/edit/main/readme.md#day_0--systemtool-setup-check-github-id-creation)

> - [Lecture_0](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lecture-topics)
> - [Lab_0](https://github.com/YishenKuma/sd_training/blob/main/readme.md#lab-session)

## **Day_0 : System/Tool Setup Check. GitHub ID creation** 
### Lecture Topics
* Chip and Package
<!---
<img src="images/Chip and package.JPG" width="400">
--->
![](images/Chip%20and%20package.JPG) 

Chip: The assembly of active and passive electronic components, along with their inetrconnections, fabricated as a single unit on a thin substrate of semiconductor material.

Package: The housing that chips are placed in. The package is then either plugged into or soldered onto the printed circuit board. 

* Wire bonding
<!---
<img src="images/wire_bond.jpg" width="400">
--->
![](images/wire_bond.jpg) 

Wire bonds are the interconnections between an integrated circuit (IC) or other semiconductor device and its packaging during semiconductor device fabrication.

* Core and IO
<!---
<img src="images/iopads.jpg" width="400">
--->
![](images/iopads.jpg) 

Core: the section of the chip where the fundamental logic of the design is placed (Macros, IPs, Etc,.)

IO: allows the communication of data between die and external components

IO Pads: acting as gateway, connecting internal signals from the core of the integrated circuit to the external pins of the chip package

* Macros and IPs
<!---
<img src="images/macro IP.jpg" width="400">
--->
![](images/macro%20IP.jpg) 

Macros: Simple custom built cell serving a sepecific funtional purpose that can be found through open sources

Foundry IPs: Macro cells developed with the intent of licencing to multiple vendor for using as building blocks in different chip designs, known as Intellectual Property 

* Communication between software and hardware
<!---
<img src="images/compilers-assemblers-translators-opener.jpg" width="400">
--->
![](images/compilers-assemblers-translators-opener.jpg) 

Compiler: reads the complete source program written in high-level language as a whole in one go and translates it into an equivalent program in assembly language

Assembler: translate the program written in assembly language into machine code represented by binary code

### Lab session

#### Steps

[Setup](scripts/github_lab0.txt)

#### Results

<!---
<img src="day0.JPG" width="850">
--->
![](day0.JPG) 

> error encountered after source standaloneHome/top.tcl

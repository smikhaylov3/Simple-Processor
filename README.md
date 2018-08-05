This is a simple processor (16 Registers with no hardware restraints on them), with an even simpler datapath.
It is implemented in Logisim. Logisim is open-source (GPL).
So feel free to try it out.
Now for a quick overview of the OP codes, condition codes and NZP bits.
The NZP bits are all stored in a single register.
These instructions modify the condition codes register: ADD, ADDI, NAND, LDR, LEA, SHF.
The BR instruction is a little different. 
This is because it uses the condition code from the CheckCC module as an input and the NZP bits for the instruction.
The BR instruction is then performed by determine the CCMatch bit for your control logic.
I have provided a sample program in the CC_ROM, OP_ROM and STATES_ROM files. Loading them into the appropriate memory
locations will allow the program to be run. The microcode.xlsx sheet will allow you to write your own program by entering 
your assembly code into subsequent rows in the first column and then simply copy and pasting the HEX column from the spreadsheet
into the main ROM (The hex will be generated automatically).

Below are some screenshots of the various components of the datapath mid-execution. Have Fun!

DATAPATH

![alt text](https://raw.githubusercontent.com/smikhaylov3/Simple-Processor/master/Datapath.png)

ALU (ARITHMETIC LOGIC UNIT)

![alt text](https://raw.githubusercontent.com/smikhaylov3/Simple-Processor/master/ALU.png)

CHECK_CC

![alt text](https://raw.githubusercontent.com/smikhaylov3/Simple-Processor/master/CheckCC.png)


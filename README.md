# WHAT THIS IS:
* This is a TTP emulator/simulator
  * TTP stands for "Taks Toy Processor" it is a processor design used for an intro to assembly programming class I took.
# TIPS AND USAGE:
* For a first time run of the emulator try: ./main Progams/PascalFinal.ram
* running ./main <yourbinary> will run your binary on the processor emulator and print output
  * output consists of the next instruction to run as read in from ram, a dump of the registers and a dump of the contents of ram
* I wrote several one liner tools for debugging along these lines under the DebugUtils directory
* To use my debugging one liners do: ./DebugUtils/<debugtool> <yourbinary>
* The above tips coupled with io redirection: > and >> bash shell script operators with grep and sed provide a good way to watch and sort through the output of the emulator on linux.
* For lower level debugging of a binary consider running the emulator in gdb and breaking on the function that implements the instruction you would like to analyze or break on a particular value of the program counter register.
* The method CompSim::ExecInstr is useful for stepping one ttp instruction at a time in gdb.
* You probably want to adjust your screen and font to fit the ram dump nicely into your screen ideally you want the output to look like a big rectangle.
* The program should exit with the pc one less than what it would be in logisim otherwise the state of the registers and ram should be identical (if not you found a bug).
* The instruction dump feature is still experimental use it at your own risk. You are better off using the gdb debugging methods described above.
# TODO:
* Clean up and reorganize.
* Create doxygen documentation.
* Create instruction set and architecture docs.
* Possibly try to add in new hardware like IO.
* Possibly try to add an internal breakpoint mechanism.
* Write more tools.
* Test and debug instruction dump mechanism.
* Test more instructions more thoroughly.
* Possibly implement more instructions.
* Possibly add user level interface for running different variations of the hardware, mainly ram size but register variations might be cool too.
* Consider making it possible for a user to install/augment the instruction set.

# DEMO:
![link to demo gif goes here](https://raw.githubusercontent.com/mehstruslehpy/Documents/master/C%2B%2B/TTPSim/TTPSimAndAsmDemo.gif)

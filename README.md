# display-a-number-on-four-seven-segment-displays
Use switch sw0, sw1, sw2 and sw3sw15 to sw0 to display a number on four seven segment displays.

Problem statements:
1. Use switch sw0, sw1, sw2 and sw3sw15 to sw0 to display a number on four seven segment displays. You can use https://github.com/Digilent/Basys3/blob/master/Projects/Abacus/src/hdl/Seg_7_Display.v for this design. Since clock is input to this module, clock will be input to problem 3 as well. Costraints for clock signal ca be given as:

set_property PACKAGE_PIN W5 [get_ports clk]
 
set_property IOSTANDARD LVCMOS33 [get_ports clk]
 
create_clock -add -name sys_clk_pin -period 10.00 -waveform {0 5} [get_ports clk]

2. Design and validate 4 bit binary adder. Use 1 bit full adder as base module. LED or seven segment can be used to show output. Tip: 4 bit adder design is given on page 35 of the verilog tutorial link given below.

3. Use this 4 bit binary adder to create a BCD adder. Both the input numbers would be 8 bit, and output would be 9 bit. Input will be taken from DIP switches (First input sw7:sw0, second input sw15:sw8) and addition output will be displayed on seven segment display.


Resources:

    https://reference.digilentinc.com/learn/programmable-logic/tutorials/basys-3-getting-started/start

    Master XDC file: https://github.com/Digilent/Basys3/tree/master/Resources/XDC
    https://ece.umd.edu/class/enee359a.S2007/verilog_tutorial.pdf
    Tools are installed at /usr/local/Vivado/2018.2 So add the right path
        export PATH=$PATH:/usr/local/Vivado/2018.2/bin

     


Tips:

    Vivado webpack is free software, can be installed on windows or Linux machine
    You may create and validate your verilog design outside lab hours. Use lab hours for validating the design on FPGA board

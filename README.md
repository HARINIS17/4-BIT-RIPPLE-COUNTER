# 4-BIT-RIPPLE-COUNTER

**AIM:**

To implement  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 Bit Ripple Counter**

A binary ripple counter consists of a series connection of complementing flip-flops (T or JK type), with the output of each flip-flop connected to the Clock Pulse input of the next higher-order flip-flop. The flip-flop holding the least significant bit receives the incoming count pulses. The diagram of a 4-bit binary ripple counter is shown in Fig. below.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/cb4b74d4-31ab-4359-95d0-d22e67daba13)

In timing diagram Q0 is changing as soon as the negative edge of clock pulse is encountered, Q1 is changing when negative edge of Q0 is encountered(because Q0 is like clock pulse for second flip flop) and so on.

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/a573a7d6-014e-4e54-93e6-e2ac9530960b)

![image](https://github.com/naavaneetha/4-BIT-RIPPLE-COUNTER/assets/154305477/85e1958a-2fc1-49bb-9a9f-d58ccbf3663c)

**Procedure**

Step1:Define clk (clock), reset (reset signal), and q (4-bit output) as inputs and outputs.

Step2:Declare a 4-bit register count to store the counter value.

Step3:Assign the value of count to the output q.

Step4:Use an always block triggered on the rising edge of clk or reset.

Step5:Check if reset is active, and if so, set count to 0000.

Step6:If reset is inactive, increment count by 1.

Step7:Allow the 4-bit register to roll over from 1111 to 0000 naturally.

**PROGRAM**

Program for 4 Bit Ripple Counter and verify its truth table in quartus using Verilog programming.

 Developed by:HARINI S
 
 RegisterNumber:24900110

module ripple(

 input clk,     
    
 input reset, 
    
 output [3:0] q     
   
);
    
 reg [3:0] count;

  assign q = count;

  if (reset)
    
 count <= 4'b0000; 
           
 else
     
 count <= count + 1;
            
 end

endmodule


**RTL LOGIC FOR 4 Bit Ripple Counter**

![Screenshot (50)](https://github.com/user-attachments/assets/b8543d40-78c3-4b5c-b39d-085f446f4a0b)


**TIMING DIGRAMS FOR 4 Bit Ripple Counter**

![Screenshot (49)](https://github.com/user-attachments/assets/7ce6406a-8c01-4a56-98bf-f253bb2788b9)


**RESULTS**

  4 Bit Ripple Counter using verilog and validating their functionality using their functional tables is implemented



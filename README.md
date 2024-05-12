# T-FLIPFLOP-POSEDGE

**AIM:**

To implement  T flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**T Flip-Flop**

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/458a68fe-2d08-4a9d-ac4f-7ae0480ce0bd)

 
This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

![image](https://github.com/naavaneetha/T-FLIPFLOP-POSEDGE/assets/154305477/cdd7fb32-539f-4b66-bb8d-f305a153c886)

 
From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

**Procedure**

Define Module: Define a Verilog module for the T flip-flop with inputs (T, CLK) and outputs (Q, Q_bar).

Declare Inputs and Outputs: Declare input and output ports for the module.

Implement Flip-Flop Logic: Write Verilog code to implement the T flip-flop logic based on its functional table. Use a synchronous always @(posedge CLK) block to trigger the flip-flop on the positive edge of the clock signal.

Simulate Using Testbench: Write a Verilog testbench to simulate the behavior of the T flip-flop under different input conditions.

Apply Input Stimuli: In the testbench, apply various combinations of input stimuli (T, CLK) to cover all possible input states.

Verify Output Behavior: Verify that the output behavior of the T flip-flop matches the expected behavior defined by its functional table.

Check for Race Conditions: Ensure that there are no race conditions or undefined states in the design by analyzing the timing and sequence of input changes.



**PROGRAM**

Developed by:Hemapriya K  RegisterNumber:212223040066

module T_FLIPFLOP( input clk, rst_n, input t,
output reg q,
output q_bar
);
always@(posedge clk) 
begin 
if(!rst_n)
 q<=0;
 else
 if(t)
 q<=~q;
 else
 q<=q;
 end
 
assign q_bar = ~q;
endmodule


**RTL LOGIC FOR FLIPFLOPS**


![325863122-e46e1a65-ea21-4034-a41f-11b20a7fc1d3](https://github.com/HemapriyaOfficial/T-FLIPFLOP-POSEDGE/assets/147114275/adfd3330-58d3-4cc6-be74-518d36b486d8)

**TIMING DIGRAMS FOR FLIP FLOPS**


![325863177-793e802c-8be8-410d-89fc-15447ab4acd1](https://github.com/HemapriyaOfficial/T-FLIPFLOP-POSEDGE/assets/147114275/66f66994-1d16-4b2e-8f1d-95539633e8e0)

**RESULT**

T flipflop using verilog and validating their functionality using their functional tables completed

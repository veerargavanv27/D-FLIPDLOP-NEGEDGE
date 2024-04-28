# D-FLIPDLOP-NEGEDGE

**AIM:**

To implement  D flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**D Flip-Flop**

D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/48c81fe8-bc3f-40e7-95e2-519fc155ad51)

This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable. The following table shows the state table of D flip-flop.

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/e5f3fda7-68ec-4a3a-a0a4-cf6f9cc4ab55)

Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as Qt+1t+1 = D

![image](https://github.com/naavaneetha/D-FLIPDLOP-NEGEDGE/assets/154305477/8592c0d8-2917-4142-91b9-d6c30dd891d2)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.

**Procedure**

1. Define Module: Define a Verilog module for the D flip-flop with inputs (D, CLK) and outputs (Q, Q_bar).

2. Declare Inputs and Outputs: Declare input and output ports for the module.

3. Implement Flip-Flop Logic: Write Verilog code to implement the D flip-flop logic based on its functional table. Use a synchronous always @(posedge CLK) block to trigger the flip-flop on the positive edge of the clock signal.

4. Simulate Using Testbench: Write a Verilog testbench to simulate the behavior of the D flip-flop under different input conditions.

5. Apply Input Stimuli: In the testbench, apply various combinations of input stimuli (D, CLK) to cover all possible input states.

6. Verify Output Behavior: Verify that the output behavior of the D flip-flop matches the expected behavior defined by its functional table.

7. Check for Race Conditions: Ensure that there are no race conditions or undefined states in the design by analyzing the timing and sequence of input changes.

**PROGRAM**
#### Developed by: VEERARAGAVAN V
#### Register number: 212223230237

```
module DFLIPFLOPNEGEDGE(D,Clock,Q,Qbar);
input D,Clock;
output reg Q,Qbar;
always @ (negedge Clock)// use negative edge clock for triggereing condition 
//compute D flipflop logic here
begin
 	Q=D;
Qbar=~D;
end
 endmodule
```

**RTL LOGIC FOR FLIPFLOPS**
![Screenshot 2024-04-18 145741](https://github.com/PremkumarG3/D-FLIPDLOP-NEGEDGE/assets/138955646/028549b0-60e1-4ccc-852c-5049c23da26b)


**TIMING DIGRAMS FOR FLIP FLOPS**
![Screenshot 2024-04-18 145703](https://github.com/PremkumarG3/D-FLIPDLOP-NEGEDGE/assets/138955646/60870f96-e222-49e3-8a30-8479e31b6fe5)


**RESULTS**


Thus the program to implement a D flipflop using verilog and validating their functionality using their functional tables.

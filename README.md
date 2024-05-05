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

1. Create a Verilog module with input and output ports.
2. Set up a testbench with input registers, wires, instantiation, initialization, and simulation.
3. Define behavioral logic to update the output based on input signals.
4. Run simulation to observe output transitions.
5. Validate simulation results against the D flip-flop's functional table.


**PROGRAM**
``` verilog

Program for flipflops and verify its truth table in quartus using Verilog programming.
Developed by: Vikamuhan reddy.N
RegisterNumber: 212223240181

module DFLIPFLOPNEGEDGE(D,Clock,reset,Q);
input D,reset,Clock;
output reg Q;
always @ (negedge Clock)
if(!reset)
Q <= 0;
else
Q <= D;
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**
![image](https://github.com/vikamuhan-reddy/D-FLIPDLOP-NEGEDGE/assets/144928933/fc92e9fe-20ff-4dad-a052-1d0b9e25b51b)


**TIMING DIGRAMS FOR FLIP FLOPS**
![image](https://github.com/vikamuhan-reddy/D-FLIPDLOP-NEGEDGE/assets/144928933/33b79fb3-d98b-4a42-9498-0e24b86e7d0c)



**RESULTS**

Thus the program to implement a D flipflop using verilog and validating their functionality using their functional tables.

# TFlipFlop-
# T-FLIPFLOP-POSEDGE
# AIM:

To implement T flipflop using verilog and validating their functionality using their functional tables

# SOFTWARE REQUIRED:

Quartus prime

# THEORY

T Flip-Flop

T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

<img width="550" height="370" alt="image" src="https://github.com/user-attachments/assets/1aae8122-9ae4-4477-93e5-fb3b85507ec3" />

This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop. The following table shows the state table of T flip-flop.

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop. Inputs Present State Next State

<img width="453" height="346" alt="image" src="https://github.com/user-attachments/assets/75acf320-9384-4cfd-ba96-552ac76b7e0e" />

From the above characteristic table, we can directly write the next state equation as Q(t+1)=T′Q(t)+TQ(t)′ ⇒Q(t+1)=T⊕Q(t)

Procedure

# PROGRAM
```
module TFlipFlop (
    input  wire clk, rst, T,
    output reg Q 	  
);

  initial begin
     Q<=1'b0;
	 end
  
  
	 always @(posedge clk or posedge rst) begin
	
        if (rst)
            Q <= 1'b0;       // Reset
        else if (T)
            Q <= ~Q;         // Toggle if T=1
        else
            Q <= Q;          // Hold if T=0
    end
endmodule
```

# Developed by:BUSHPIKA C
# RegisterNumber:25007434

# RTL LOGIC FOR FLIPFLOPS
<img width="1920" height="1080" alt="Screenshot 2025-12-15 191319" src="https://github.com/user-attachments/assets/157b4233-e1c3-473d-a284-4915e1ee2d48" />


# TIMING DIGRAMS FOR FLIP FLOPS
<img width="1920" height="1080" alt="Screenshot 2025-12-15 191649" src="https://github.com/user-attachments/assets/b9325e40-9613-464e-aaab-b1eea83d09f1" />

# RESULTS
Thus the program has been executed succesfully

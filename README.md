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


**PROGRAM**

Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by:Buvaneshwari.R

RegisterNumber:24900165.

module exp9(input clk, rst_n,input t,
output reg q,
output q_bar
);
always @(posedge clk)
begin 
if(!rst_n)
q<=0;
else 
begin 
q<=(t?~q:q);
end 
end 
assign q_bar = ~q;
endmodule 


**RTL LOGIC FOR FLIPFLOPS**

![Screenshot 2024-12-25 162135](https://github.com/user-attachments/assets/7b0e2cd7-5acf-4474-9046-68da254c7ec3)




**TIMING DIGRAMS FOR FLIP FLOPS**

![Screenshot 2024-12-25 162421](https://github.com/user-attachments/assets/7b2f42e6-866a-4cb4-a178-c2603279b3d6)


**RESULTS**

T flipflop is studied and verified successfully using Quartus software.

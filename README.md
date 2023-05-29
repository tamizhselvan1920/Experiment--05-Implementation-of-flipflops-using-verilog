# Experiment--05-Implementation-of-flipflops-using-verilog
### AIM: To implement all the flipflops using verilog and validating their functionality using their functional tables
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 
SR Flip-Flop
SR flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, SR latch operates with enable signal. The circuit diagram of SR flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167910294-bb550548-b1dc-4cba-9044-31d9037d476b.png)

 
This circuit has two inputs S & R and two outputs Qtt & Qtt’. The operation of SR flipflop is similar to SR Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of SR flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167910648-ced88e69-869c-42e2-9718-a285a3902446.png)


Here, Qtt & Qt+1t+1 are present state & next state respectively. So, SR flip-flop can be used for one of these three functions such as Hold, Reset & Set based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of SR flip-flop.
Present Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167908180-5fc9d589-1cb5-41f5-b2c8-927e04f5f387.png)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. The three variable K-Map for next state, Qt+1t+1 is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167908214-25b30a54-db20-4bcb-9385-5f93a1982a09.png)

 
The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=S+R′Q(t)Q(t+1)=S+R′Q(t)


### D Flip-Flop
D flip-flop operates with only positive clock transitions or negative clock transitions. Whereas, D latch operates with enable signal. That means, the output of D flip-flop is insensitive to the changes in the input, D except for active transition of the clock signal. The circuit diagram of D flip-flop is shown in the following figure.
 
This circuit has single input D and two outputs Qtt & Qtt’. The operation of D flip-flop is similar to D Latch. But, this flip-flop affects the outputs only when positive transition of the clock signal is applied instead of active enable.
The following table shows the state table of D flip-flop.
![image](https://user-images.githubusercontent.com/36288975/167908342-e03f0cbb-5958-43bb-b74a-5e3ec2341675.png)

![image](https://user-images.githubusercontent.com/36288975/167910325-aeef0739-0a54-40e2-bebd-6f5fa0cad10e.png)



Therefore, D flip-flop always Hold the information, which is available on data input, D of earlier positive transition of clock signal. From the above state table, we can directly write the next state equation as
Qt+1t+1 = D



![image](https://user-images.githubusercontent.com/36288975/167908850-d39d07ba-7f9d-490a-b9f2-274e189fd047.png)

Next state of D flip-flop is always equal to data input, D for every positive transition of the clock signal. Hence, D flip-flops can be used in registers, shift registers and some of the counters.


### JK Flip-Flop
JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.
![image](https://user-images.githubusercontent.com/36288975/167910378-d2d984a7-2815-4d17-8c41-ee4bdf59ec24.png) 

 
This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs.
The following table shows the state table of JK flip-flop.


![image](https://user-images.githubusercontent.com/36288975/167908575-59c35afb-50d3-46a2-888c-47478a3179d5.png)

Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop.
Present Inputs	Present State	Next State

![image](https://user-images.githubusercontent.com/36288975/167908664-c854ffe9-0bd3-44c2-bfa6-e53928181c69.png)


By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
 
 ![image](https://user-images.githubusercontent.com/36288975/167908688-fa93c3e9-8323-4864-947d-c11d163d5a90.png)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is
Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)



### T Flip-Flop
T flip-flop is the simplified version of JK flip-flop. It is obtained by connecting the same input ‘T’ to both inputs of JK flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of T flip-flop is shown in the following figure.

![image](https://user-images.githubusercontent.com/36288975/167911534-5f3c445d-bc68-46e2-9a9c-7efce5febc60.png)



This circuit has single input T and two outputs Qtt & Qtt’. The operation of T flip-flop is same as that of JK flip-flop. Here, we considered the inputs of JK flip-flop as J = T and K = T in order to utilize the modified JK flip-flop for 2 combinations of inputs. So, we eliminated the other two combinations of J & K, for which those two values are complement to each other in T flip-flop.
The following table shows the state table of T flip-flop.



Here, Qtt & Qt+1t+1 are present state & next state respectively. So, T flip-flop can be used for one of these two functions such as Hold, & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of T flip-flop.
Inputs	Present State	Next State


![image](https://user-images.githubusercontent.com/36288975/167909015-53aa9450-3f28-4202-887a-79d88228f8a0.png)

From the above characteristic table, we can directly write the next state equation as
Q(t+1)=T′Q(t)+TQ(t)′
⇒Q(t+1)=T⊕Q(t)

### Procedure

1.Create a project with required entities.
2.Create a module along with respective file name. 
3.Run the respective programs for the given boolean equations.
4.Run the module and get the respective RTL outputs.
5.Create university program(VWF) for getting timing diagram.
6.Give the respective inputs for timing diagram and obtain the results.


### PROGRAM

#### SR FLIP FLOPS:
```

*/
Program for flipflops  and verify its truth table in quartus using Verilog programming.
Developed by: tamizh selvan R
RegisterNumber: 212222230158 
module de05(S,R,CLK,Q,QBAR);
input S,R,CLK;
output Q,QBAR;
wire X,Y;
nand(X,S,CLK);
nand(Y,R,CLK);
nand(Q,X,QBAR);
nand(QBAR,Y,Q);
endmodule
*/
```

#### D FLIP FLOPS:
```

/*
module de052(D,CLK,Q,QBAR);
input D,CLK;
output Q,QBAR;
assign DBAR=~D;
wire X,Y;
nand(X,D,CLK);
nand(Y,DBAR,CLK);
nand(Q,X,QBAR);
nand(QBAR,Y,Q);
endmodule
/*

```
#### T FLIP FLOPS:
```
/*
module de54(T,CLK,Q,QBAR);
input T,CLK;
output Q,QBAR;
wire S,R;
nand(S,T,CLK,QBAR);
nand(R,T,CLK,Q);
nand(Q,S,QBAR);
nand(QBAR,R,Q);
endmodule
/*


### RTL LOGIC FOR FLIPFLOPS 
```

![238019215-9d772ad9-0312-4ada-8269-e198622e5d87](https://github.com/tamizhselvan1920/Experiment--05-Implementation-of-flipflops-using-verilog/assets/121148386/48b28ef6-7486-4d19-a31c-76d1687a0486)

![238019319-4bfa1d58-4566-4423-82a7-c764b09fd128](https://github.com/tamizhselvan1920/Experiment--05-Implementation-of-flipflops-using-verilog/assets/121148386/18ecf695-53a2-4632-a8cc-5dcf64b52205)



![238019426-0d4fff2e-7405-4e99-bc3d-3b3a7339041f](https://github.com/tamizhselvan1920/Experiment--05-Implementation-of-flipflops-using-verilog/assets/121148386/d3221c51-71fb-4b77-a2ff-2433b50d83e1)


![238019616-f02c65d0-555d-4635-a428-63f9057e8bd6](https://github.com/tamizhselvan1920/Experiment--05-Implementation-of-flipflops-using-verilog/assets/121148386/1d90e976-9aa9-49f2-812f-d484a5421632)


### TIMING DIGRAMS FOR FLIP FLOPS 


![238019237-dce48568-9ab7-4a6f-98b3-5a5876e07f4b](https://github.com/tamizhselvan1920/Experiment--05-Implementation-of-flipflops-using-verilog/assets/121148386/155b2f1b-bcd3-4a5b-93c7-a4a505a2aec6)


![238019336-538c65a8-2395-47ec-9ad1-58ae045a80c3](https://github.com/tamizhselvan1920/Experiment--05-Implementation-of-flipflops-using-verilog/assets/121148386/2d77cde8-a77c-4480-bf93-a7c7c4edffb9)


![238019455-caea6ee6-eb2c-4121-a4c8-0bb5438a557a](https://github.com/tamizhselvan1920/Experiment--05-Implementation-of-flipflops-using-verilog/assets/121148386/06c62766-2ce8-4018-a5d5-208115ac14e9)

![238019659-8347cecd-c87b-4db5-8a74-79e8cbef64a1](https://github.com/tamizhselvan1920/Experiment--05-Implementation-of-flipflops-using-verilog/assets/121148386/7f3780c6-92dd-44d5-a744-032e1f024a4a)



### RESULTS 
 Hence all the flipflops are implemented using verilog and their functionality has been validated using their functional tables.

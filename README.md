# Swapping-Three-Numbers
Aim
To design and simulate a Verilog HDL code for swapping the values of three numbers without using any temporary variables, and verify the correctness of the swapping operation through a testbench using the Vivado 2023.1 simulation environment.

Apparatus Required
Vivado 2023.1 or equivalent Verilog simulation tool.

Procedure
Launch Vivado 2023.1:

Open Vivado and create a new project.
Write the Verilog Code for Swapping:

Write the Verilog code that swaps the values of three numbers (a, b, and c) using basic arithmetic or bitwise operations without using temporary variables.
Create the Testbench:

Write a testbench to simulate the swapping operation. The testbench should initialize three numbers, trigger the swapping module, and check if the values are swapped correctly.
Add the Verilog Files:

Add the Verilog module and the testbench file to the Vivado project.
Run Simulation:

Run the behavioral simulation in Vivado to verify the swapping operation.
Observe the Waveforms:

Examine the waveform to confirm that the values of the three numbers are swapped as expected.
Save and Document Results:

Capture the waveform output and include the results in your report for verification.

Verilog Code:

Blocking using input and output variable:

```module swap_3_num(input[7:0]a_in,
                  input[7:0]b_in,
                  input[7:0]c_in,
                  output reg[7:0]a_out,
                  output reg[7:0]b_out,
                  output reg[7:0]c_out    );
                  
                  always@(*) 
                  begin
                  a_out=b_in;
                  b_out=c_in;
                  c_out=a_in;
                  end
endmodule
```
Non-blocking using input and output variable:

```module swap_3_num(input[7:0]a_in,
                  input[7:0]b_in,
                  input[7:0]c_in,
                  output reg[7:0]a_out,
                  output reg[7:0]b_out,
                  output reg[7:0]c_out    );
                  
                  always@(*) 
                  begin
                  a_out<=b_in;
                  b_out<=c_in;
                  c_out<=a_in;
                  end
endmodule
```
Blocking without using input and output variable:
```
module swap_3_numbers;
reg[7:0]a,b,c;
initial
  begin
  a=4'd8;b=4'd7;c=4'd6;
  end
always@(*)
begin

a=b;
b=c;
c=a;

end

endmodule
```
Non-Blocking without using input and output variable:
```
module swap_3_numbers;
reg[7:0]a,b,c;
initial
  begin
  a=4'd8;b=4'd7;c=4'd6;
  end
always@(*)
begin

a<=b;
b<=c;
c<=a;

end
endmodule
```

Output

Blocking and Non-Blocking using input and output variable:

![Screenshot (126)](https://github.com/user-attachments/assets/c6b8e95a-7322-4f45-a3df-c5c820c821b1)

Blocking and Non-Blocking without using input and output variable:

![Screenshot (127)](https://github.com/user-attachments/assets/5397dccc-6deb-4d9d-a499-3a48d2b59f88)




Conclusion
In this experiment, a Verilog HDL code for swapping three numbers was designed and successfully simulated

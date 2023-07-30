Verilog's code is based on modules, each module has a module name, inputs and outputs

```verilog
module example (
     input a, input b, input c, output y;
);
     // Module Description
endmodule
```

We can also define range of Bit

```verilog
module example (
// Range-end - Range-start + 1, so 31-0+1 = 32 Bit
     input [31:0]a, input [31:0]b, input [31:0]c, output y;
);
     // Module Description
endmodule
```

We can also import other modules from a other file with `include` and use it.

```verilog
module small (
     input A,
     input B,
     output Y;
);
endmodule
```

```verilog
`include "small.v"

module example (
     input A, input SEL, input C, output Y;
);
     wire n1;
     small i_first (
          .A(A),
          .B(SEL),
          .Y(n1)
     )
     small i_second(
          .A(n1),
          .B(C),
          .Y(Y);
     )
endmodule
```

We can use `assign` to assign variable
![[Pasted image 20230409165827.png]]

numbers in Verilog:
![[Pasted image 20230409171855.png]]

The statement is executed only when the event specified in the sensitivity list occurs. In this example, the statement is q <= d (pronounced “q gets d”). It's similar as =. With a * inside it, it will always be executed 
```verilog
// posedge is like a transition from 0 to 1, negedge the oposit transition from 1 to 0. 
always @ (posedge clk)
	q <= d
```

`case`
![[Pasted image 20230409172109.png]]

- Testbench
```verilog
initial begin
	a = 0;
	#10 //wait 10 seconds
	a = 1;
	$display("printf() style message")
end
```
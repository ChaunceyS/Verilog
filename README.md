# Verilog
VerilogHDL
module FCFC(   
	 input a,
    input b,
    input c,
    input d,
    input e,
	 output reg g,
    output reg f);
initial g=1'b1;
always@(a or b or d or e or g)
begin
	case(g)
		a&b&c:f=1'b1;
		a&b&d:f=1'b1;
		a&b&e:f=1'b1;
		a&c&d:f=1'b1;
		a&c&e:f=1'b1;
		a&d&e:f=1'b1;
		b&c&d:f=1'b1;
		b&c&e:f=1'b1;
		b&d&e:f=1'b1;
		c&d&e:f=1'b1;
		default:f=1'b0;
	endcase
end
endmodule

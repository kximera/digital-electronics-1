# Lab 5: Jesús Santos Gravalosa

### D & T Flip-flops

1. Screenshot with simulated time waveforms. Try to simulate both D- and T-type flip-flops in a single testbench with a maximum duration of 350 ns, including reset. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

 ![image](https://user-images.githubusercontent.com/63504192/225099153-2bb45edc-1a57-4287-b5ad-517a2696f554.png)

### JK Flip-flop

1. Listing of VHDL architecture for JK-type flip-flop. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture Behavioral of jk_ff_rst is
    signal sig_q : std_logic;
begin
    jk_ff_rst : process (clk)
     begin
        if rising_edge(clk) then
            if (rst = '1') then
                sig_q <= '0';
	    else
                if (J = '0' and K = '0') then
                    sig_q <= sig_q;
                elsif (J = '0' and K = '1') then
                    sig_q <= '0';
                elsif (J = '1' and K = '0') then
                    sig_q <= '1';
                else
               	    sig_q <= not sig_q;
                end if;
             end if;
        end if;
    end process jk_ff_rst;
    q     <= sig_q;
    q_bar <= not sig_q;
end architecture Behavioral;
```

### Shift register

1. Image of `top` level schematic of the 4-bit shift register. Use four D-type flip-flops and connect them properly. The image can be drawn on a computer or by hand. Always name all inputs, outputs, components and internal signals!

![asemeunpt](https://user-images.githubusercontent.com/63504192/225101201-cb115239-02c8-4d84-abce-284c8c51d9e4.jpg)

   

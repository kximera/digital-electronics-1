# Lab 6: Jesús Santos Gravalosa

### Bidirectional counter

1. Listing of VHDL code of the completed process `p_cnt_up_down`. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
  p_cnt_up_down : process (clk) is
	begin
	
	if rising_edge(clk) then
		if (rst = '1') then           
			sig_cnt <= (others => '0');   
		elsif (en = '1') then       
			if (cnt_up = '1') then       
				sig_cnt <= sig_cnt + 1;  
			else
				sig_cnt <= sig_cnt - 1;   
			end if;
		end if;
	end if;
	
	end process p_cnt_up_down;
```

2. Screenshot with simulated time waveforms. Test: (a) reset, (b) counter direction, (c) enable. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

![image](https://user-images.githubusercontent.com/63504192/226735250-b98026f3-3acf-445b-a746-1f527401158c.png)


 

### Two counters

1. Image of the top layer structure including both counters, ie a 4-bit bidirectional counter from *Part 4* and a 12-bit counter with a 10 ms time base from *Experiments on your own*. The image can be drawn on a computer or by hand. Always name all inputs, outputs, components and internal signals!

  ![fotito](https://user-images.githubusercontent.com/63504192/226735520-41639d1a-d835-4440-8356-a5a06fd38693.jpg)


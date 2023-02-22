# Lab 2: JESUS SANTOS

### 2-bit comparator

1. Karnaugh maps for other two functions of 2-bit comparator:

   Greater than:

  ![mayor](https://user-images.githubusercontent.com/63504192/220477010-545bdf4c-b35f-40d9-96c4-0ed596df7c27.jpg)



   Less than:
![menor](https://user-images.githubusercontent.com/63504192/220476893-8479ebda-34ea-4761-b08d-5065ceb73c59.jpg)

   

2. Mark the largest possible implicants in the K-map and according to them, write the equations of simplified SoP (Sum of the Products) form of the "greater than" function and simplified PoS (Product of the Sums) form of the "less than" function.

   
![funciones](https://user-images.githubusercontent.com/63504192/220477093-7750c5c2-60cf-4572-9c4c-a5aa4a8c9396.jpg)


### 4-bit comparator

1. Listing of VHDL stimulus process from testbench file (`testbench.vhd`) with at least one assert (use BCD codes of your student ID digits as input combinations). Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

   Last two digits of my student ID: **250930**

```vhdl
    p_stimulus : process
    begin
        -- Report a note at the beginning of stimulus process
        report "Stimulus process started";

        -- First test case
        s_b <= "0011";--3
        s_a <= "0000";--0
        wait for 100 ns;
        -- Expected output
        assert ((s_B_greater_A = '1') and
                (s_B_equals_A  = '0') and
                (s_B_less_A    = '0'))
        -- If false, then report an error
        report "Input combination COMPLETE_THIS_TEXT FAILED" severity error;

        -- Report a note at the end of stimulus process
        report "Stimulus process finished";
        wait;
    end process p_stimulus;
```

2. Link to your public EDA Playground example:

   [https://www.edaplayground.com/...][(https://www.edaplayground.com/...](https://www.edaplayground.com/x/mZdC))

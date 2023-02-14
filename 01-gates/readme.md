# Lab 1: Jesus Santos

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):

 ![xexen](https://user-images.githubusercontent.com/63504192/218881200-f1b36a25-b5bb-46b0-b741-56af998ed44a.jpg)


2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of gates is
begin
   f_orig_o <= (not(b_i) and a_i) or (c_i and not(b_i or not(a_i)));
   f_nand_o <= not(not(not(b_i) and a_i) and not(not(c_i) and not(b_i) and a_i));
   f_nor_o  <= not(b_i or not(a_i)) or not(not(c_i) or (b_i or not(a_i)))
end architecture dataflow;

```

3. Complete table with logic functions' values:

   | **c** | **b** |**a** | **f_ORIG** | **f_(N)AND** | **f_(N)OR** |
   | :-: | :-: | :-: | :-: | :-: | :-: |
   | 0 | 0 | 0 | 0 | 0 | 0 |
   | 0 | 0 | 1 | 1 | 1 | 1 |
   | 0 | 1 | 0 | 0 | 0 | 0 |
   | 0 | 1 | 1 | 0 | 0 | 0 |
   | 1 | 0 | 0 | 0 | 0 | 0 |
   | 1 | 0 | 1 | 1 | 1 | 1 |
   | 1 | 1 | 0 | 0 | 0 | 0 |
   | 1 | 1 | 1 | 0 | 0 | 0 |

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![image](https://user-images.githubusercontent.com/63504192/218883084-33e1946b-744e-4eaf-879f-c3045405090a.png)

2. Link to your public EDA Playground example:

   [https://www.edaplayground.com/...](https://www.edaplayground.com/x/pQnw)

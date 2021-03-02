# Digital-Electronics-1

https://github.com/AnaSampaio13/Digital-Electronics-1

## Exercise 1

![Nexys A7 board](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex1.PNG)
```
----------------------------------------------------------------------------------

## Exercise 2
```VHDL
----------------------------------------------------------------------------------
###**VHDL architecture**
-- Company: 
-- Engineer: 
-- 
-- Create Date: 02/26/2021 04:37:06 PM
-- Design Name: 
-- Module Name: mux_2bit_4to1 - Behavioral
-- Project Name: 
-- Target Devices: 
-- Tool Versions: 
-- Description: 
-- 
-- Dependencies: 
-- 
-- Revision:
-- Revision 0.01 - File Created
-- Additional Comments:
-- 
----------------------------------------------------------------------------------


library IEEE;
use IEEE.STD_LOGIC_1164.ALL;

-- Uncomment the following library declaration if using
-- arithmetic functions with Signed or Unsigned values
--use IEEE.NUMERIC_STD.ALL;

-- Uncomment the following library declaration if instantiating
-- any Xilinx leaf cells in this code.
--library UNISIM;
--use UNISIM.VComponents.all;

entity mux_2bit_4to1 is

    port(
        a_i    : in std_logic_vector(2 - 1 downto 0);
        b_i    : in std_logic_vector(2 - 1 downto 0);
        c_i    : in std_logic_vector(2 - 1 downto 0);
        d_i    : in std_logic_vector(2 - 1 downto 0);
        sel_i  : in std_logic_vector(2 - 1 downto 0);
        f_o    : out std_logic_vector(2 - 1 downto 0)    
    );

end mux_2bit_4to1;

architecture Behavioral of mux_2bit_4to1 is

begin

    f_o <= a_i when (sel_i ="00") else
           b_i when (sel_i ="01") else
           c_i when (sel_i ="10") else
           d_i;
           

end architecture Behavioral;
```
--------------------------------------------------------------------------------------
```VHDL
--------------------------------------------------------------------------------------
###**VHDL testbench**
library IEEE;
use IEEE.STD_LOGIC_1164.ALL;



entity tb_mux_2bit_4to1 is
-- Entity of testbench is always empty
end tb_mux_2bit_4to1;



architecture Behavioral of tb_mux_2bit_4to1 is



-- Local signals
signal s_a : std_logic_vector(2 - 1 downto 0);
signal s_b : std_logic_vector(2 - 1 downto 0);
signal s_c : std_logic_vector(2 - 1 downto 0);
signal s_d : std_logic_vector(2 - 1 downto 0);
signal s_sel : std_logic_vector(2 - 1 downto 0);
signal s_f : std_logic_vector(2 - 1 downto 0);

begin



uut_mux_2bit_4tol : entity work.mux_2bit_4to1
port map(
a_i => s_a,
b_i => s_b,
c_i => s_c,
d_i => s_d,
sel_i => s_sel,
f_o => s_f
);



p_stimulus : process
begin

report "Stimulus process started" severity note;

s_d <= "11"; s_c <= "10"; s_b <= "01"; s_a <= "00";
s_sel <= "00"; wait for 100 ns;
s_sel <= "01"; wait for 100 ns;
s_sel <= "10"; wait for 100 ns;
s_sel <= "11"; wait for 100 ns;
end process p_stimulus;

end architecture Behavioral;
```
--------------------------------------------------------
###**Screenshot**

![Waveforms](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex2.jpg)

--------------------------------------------------------
## Exercise 3 

**Step 1**
![Step 1](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.1.jpg)

**Step 2**
![Step 2](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.2.jpg)

**Step 3**
![Step 3](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.3.jpg)

**Step 4**
![Step 4](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.4.jpg)

**Step 5**
![Step 5](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.5.jpg)

**Step 6**
![Step 6](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.6.jpg)

**Step 7**
![Step 7](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.7.jpg)

**Step 8**
![Step 8](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.8.jpg)

**Step 9**
![Step 9](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.9.jpg)

**Step 10**
![Step 10](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.10.jpg)

**Step 11**
![Step 11](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.11.jpg)

**Step 12**
![Step 12](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.12.jpg)

**Step 13**
![Step 13](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.13.jpg)

**Step 14**
![Step 14](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.14.jpg)

**Step 15**
![Step 15](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.15.jpg)

**Step 16**
![Step 16](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.16.jpg)

**Step 17**
![Step 17](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.17.PNG)

**Step 18**
![Step 18](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/03-vivado/Pictures/Ex3.18.PNG)

#Digital-Electronics-1

https://github.com/AnaSampaio13/Digital-Electronics-1

##Exercise 1

![7-segment displays on Nexys A7 board](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/04-segment/Pictures/Capturar.PNG)

--------------------------------------------------------------------------------
###**Truth table**
**Hex** | **Inputs** | **A** | **B** | **C** |	**D** |	**E** |	**F** |	**G**
--- | --- | --- | --- | --- | --- | --- | --- | --- 
0 |	0000 | 0 | 0 | 0 | 0 | 0 | 0 | 1
1 | 0001 | 1 | 0 | 0 | 1 | 1 | 1 | 1
2 | 0010 | 0 | 0 | 1 | 0 | 0 | 1 | 0	
3 |	0011 | 0 | 0 | 0 | 0 | 1 | 1 | 0
4 |	0100 | 1 | 0 | 0 | 1 | 1 | 0 | 0
5 |	0101 | 0 | 1 | 0 | 0 | 1 | 0 | 0
6 |	0110 | 0 | 1 | 0 | 0 | 0 | 0 | 0
7 |	0111 | 0 | 0 | 0 | 1 | 1 | 1 | 1
8 |	1000 | 0 | 0 | 0 | 0 | 0 | 0 | 0
9 |	1001 | 0 | 0 | 0 | 0 | 1 | 0 | 0
A |	1010 | 0 | 0 | 0 | 1 | 0 | 0 | 0
B |	1011 | 1 | 1 | 0 | 0 | 0 | 0 | 0
C |	1100 | 0 | 1 | 1 | 0 | 0 | 0 | 1
D |	1101 | 1 | 0 | 0 | 0 | 0 | 1 | 0
E |	1110 | 0 | 1 | 1 | 0 | 0 | 0 | 0
F |	1111 | 0 | 1 | 1 | 1 | 0 | 0 | 0
----------------------------------------------------------------------------------

##Exercise 2
```VHDL
----------------------------------------------------------------------------------

###**VHDL architecture**

-- Company: 
-- Engineer: 
-- 
-- Create Date: 03/05/2021 07:45:19 PM
-- Design Name: 
-- Module Name: hex_7seg - Behavioral
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

entity hex_7seg is
    Port ( 
         hex_i : in STD_LOGIC_VECTOR (4 - 1 downto 0);
         seg_o : out STD_LOGIC_VECTOR (7 - 1 downto 0)
     );
end hex_7seg;

architecture Behavioral of hex_7seg is
begin

    --------------------------------------------------------------------
    -- p_7seg_decoder:
    -- A combinational process for 7-segment display (Common Anode)
    -- decoder. Any time "hex_i" is changed, the process is "executed".
    -- Output pin seg_o(6) controls segment A, seg_o(5) segment B, etc.
    --       segment A
    --        | segment B
    --        |  | segment C
    --        |  |  |   ...   segment G
    --        +-+|+-+          |
    --          |||            |
    -- seg_o = "0000001"-------+
    --------------------------------------------------------------------
    p_7seg_decoder : process(hex_i)
    begin
        case hex_i is
            when "0000" =>
                seg_o <= "0000001";     -- 0
            when "0001" =>
                seg_o <= "1001111";     -- 1
            when "0010" =>
                seg_o <= "0010010";     -- 2
            when "0011" =>
                seg_o <= "0000110";     -- 1
            when "0100" =>
                seg_o <= "1001100";     -- 1                
            when "0101" =>
                seg_o <= "0100100";     -- 1                
            when "0110" =>
                seg_o <= "0100000";     -- 1
            when "0111" =>
                seg_o <= "0001111";     -- 8
            when "1000" =>
                seg_o <= "0000000";     -- 1
            when "1001" =>
                seg_o <= "0000100";     -- 1
            when "1010" =>
                seg_o <= "0001000";     -- 1
            when "1011" =>
                seg_o <= "1100000";     -- 1
            when "1100" =>
                seg_o <= "0110001";     -- 1
            when "1101" =>
                seg_o <= "1000010";     -- 1                                                                                
            when "1110" =>
                seg_o <= "0110000";     -- E
            when others =>
                seg_o <= "0111000";     -- F
        end case;
    end process p_7seg_decoder;

end architecture Behavioral;
--------------------------------------------------------------------------------------
###**VHDL testbench**

-- Company: 
-- Engineer: 
-- 
-- Create Date: 03/05/2021 08:23:41 PM
-- Design Name: 
-- Module Name: tb_hex_7seg - Behavioral
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

entity tb_hex_7seg is
--  Port ( );
end tb_hex_7seg;

architecture Behavioral of tb_hex_7seg is

  signal    s_hex        : std_logic_vector(4 - 1 downto 0);
  signal    s_seg        : std_logic_vector(7 - 1 downto 0);

  
begin  

uut_hex_7seg : entity work.hex_7seg
        port map(
            hex_i           => s_hex,
            seg_o           => s_seg
          
        );
    p_stimulus : process
    begin
        -- Report a note at the beginning of stimulus process
        report "Stimulus process started" severity note;


        s_hex <= "0000"; wait for 100 ns;
        s_hex <= "0001"; wait for 100 ns;
        s_hex <= "0010"; wait for 100 ns;
        s_hex <= "0011"; wait for 100 ns;
        s_hex <= "0100"; wait for 100 ns;
        s_hex <= "0101"; wait for 100 ns;
        s_hex <= "0110"; wait for 100 ns;
        s_hex <= "0111"; wait for 100 ns;
        s_hex <= "1000"; wait for 100 ns;
        s_hex <= "1001"; wait for 100 ns;
        s_hex <= "1010"; wait for 100 ns;
        s_hex <= "1011"; wait for 100 ns;
        s_hex <= "1100"; wait for 100 ns;
        s_hex <= "1101"; wait for 100 ns;
        s_hex <= "1110"; wait for 100 ns;
        s_hex <= "1111"; wait for 100 ns;
        
        
        
        report "Stimulus process finished" severity note;
        wait;
        
    end process p_stimulus;        

end Behavioral;
-------------------------------------------------------------------
###**Listing of VHDL code**

```
-------------------------------------------------------------------
###**Screenshot**

![Waveforms](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/04-segment/Pictures/Ex2.jpg)
-------------------------------------------------------------------

##Exercise 3
-------------------------------------------------------------------

###**Truth table for LEDs**
**Hex**	| **Inputs** | **LED4** | **LED5** | **LED6** | **LED7**
--- | --- | --- | --- | --- | ---
0 | 0000 | 1 | 0 | 0 | 0	
1 | 0001 | 0 | 0 | 1 | 1	
2 | 0010 | 0 | 0 | 0 | 1		
3 | 0011 | 0 | 0 | 1 | 0	
4 | 0100 | 0 | 0 | 0 | 1	
5 | 0101 | 0 | 0 | 1 | 0	
6 | 0110 | 0 | 0 | 0 | 0	
7 | 0111 | 0 | 0 | 1 | 0	
8 | 1000 | 0 | 0 | 0 | 1	
9 | 1001 | 0 | 0 | 1 | 0	
A | 1010 | 0 | 1 | 0 | 0	
B | 1011 | 0 | 1 | 1 | 0	
C | 1100 | 0 | 1 | 0 | 0	
D | 1101 | 0 | 1 | 1 | 0	
E | 1110 | 0 | 1 | 0 | 0	
F | 1111 | 0 | 1 | 1 | 0	
----------------------------------------------------------------------
###**Screenshot**

![Waveforms]()
#Digital-Electronics-1

https://github.com/AnaSampaio13/Digital-Electronics-1

##Exercise 1
--------------------------------------------------------------------------------
###**Characteristic equations** 

q_{n+1}^D =&~ \\
q_{n+1}^{JK} =&\\
q_{n+1}^T =&\\
--------------------------------------------------------------------------------
###**Truth tables**


   | **clk** | **d** | **q(n)** | **q(n+1)** | **Comments** |
   | :-: | :-: | :-: | :-: | :-- |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 0 | 0 | 0 | Reset |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 0 | 1 | 0 | Reset |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 1 | 0 | 1 | Set |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 1 | 1 | 1 | Set |   

   | **clk** | **j** | **k** | **q(n)** | **q(n+1)** | **Comments** |
   | :-: | :-: | :-: | :-: | :-: | :-- |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 0 | 0 | 0 | 0 | No change |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 0 | 0 | 1 | 1 | No change |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 0 | 1 | 0 | 0 | Reset |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 0 | 1 | 1 | 0 | Reset |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 1 | 0 | 0 | 1 | Set |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 1 | 0 | 1 | 1 | Set |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 1 | 1 | 0 | 1 | Toggles |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 1 | 1 | 1 | 0 | Toggles |

   | **clk** | **t** | **q(n)** | **q(n+1)** | **Comments** |
   | :-: | :-: | :-: | :-: | :-- |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 0 | 0 | 0 | No change |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 0 | 1 | 1 | No change |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 1 | 0 | 1 | Toggles |
   | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/07-ffs/Pictures/Ex1.PNG) | 1 | 1 | 0 | Toggles |
------------------------------------------------------------------------------------   
##Exercise 2
```VHDL
----------------------------------------------------------------------------------
###**Listing of VHDL code of the process**
------------------------------------------------------------------------  

-------------------------------------------------------------------
###**Listing of VHDL testbench file**
------------------------------------------------------------------------

``` 
-----------------------------------------------------------------------
###**Screenshot**

![Waveforms]() 
-------------------------------------------------------------------------  
##Exercise 3
```VHDL
----------------------------------------------------------------------------------
###**Listing of VHDL code of the process**
------------------------------------------------------------------------  

-------------------------------------------------------------------
###**Listing of VHDL clock, reset and stimulus processes from the testbench files**
------------------------------------------------------------------------

``` 
-----------------------------------------------------------------------
###**Screenshot**

![Waveforms]() 
-------------------------------------------------------------------------
##Exercise 4

![Image of the shift register schematic]()
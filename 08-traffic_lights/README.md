#Digital-Electronics-1

https://github.com/AnaSampaio13/Digital-Electronics-1

##Exercise 1
--------------------------------------------------------------------------------
###**State table** 

| **Input P** | `0` | `0` | `1` | `1` | `0` | `1` | `0` | `1` | `1` | `1` | `1` | `0` | `0` | `1` | `1` | `1` |
| :-- | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| **Clock** | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) | ![rising](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.1.PNG) |
| **State** | A | A | B | C | C | D | A | B | C | D | B | B | B | C | D | B |
| **Output R** | `0` | `0` | `0` | `0` | `0` | `1` | `0` | `0` | `0` | `1` | `0` | `0` | `0` | `0` | `1` | `0` |

###**Image**

![Nexys A7 board](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.2.PNG)
![Nexys A7 board](https://github.com/AnaSampaio13/Digital-Electronics-1/blob/main/08-traffic_lights/Pictures/Ex1.3.PNG)

|**RGB LED** | **Artix-7 pin names** | **Red** | **Yellow** | **Green**| 
|:-- | :-- | :-- | :-- | :--|
|LD16 | N15, M16, R12 | ```1,0,0``` | ```1,1,0``` | ```0,1,0```|
|LD17 | N16, R11, G14 | ```1,0,0``` | ```1,1,0``` | ```0,1,0```|
---------------------------------------------------------------------------------
##Exercise 2
---------------------------------------------------------------------------------
###**State diagram**

---------------------------------------------------------------------------------
###**Listing of VHDL code of sequential process**
```VHDL

---------------------------------------------------------------------------------
###**Listing of VHDL code of combinatorial process**

```
---------------------------------------------------------------------------------
###**Screenshot(s)**

![Screenshot]()
---------------------------------------------------------------------------------
##Exercise 3
---------------------------------------------------------------------------------
###**State table**

---------------------------------------------------------------------------------
###**State diagram**

---------------------------------------------------------------------------------
###**Listing of VHDL code of sequential process**
```VHDL


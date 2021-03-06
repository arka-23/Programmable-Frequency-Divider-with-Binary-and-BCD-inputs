# Design for a Programmable Frequency Divider (50 % duty cycle) with Binary and BCD inputs (with FPGA implementation)
This repository contains the design and simulation of a programmable frequency divider (50 % duty cycle)  using 
- Asynchronous decade down counter and 
- Asynchronous binary down counter 

by cascading modified MC 4316 and MC 4318 (4 bit) IC circuits designed as hierarchical blocks in Multisim, which is fully functional with proper outputs.
The above design which gives a 50% duty cycle when used as frequency divider circuit, has been coded using Verilog
HDL, and the counter circuit simulated on a Nexus 4 - Arctix 7 FPGA board to verify results.

# Table of Contents
 - [Abstract](#abstract) 
 - [Multisim Implementation](#multisim-implementation)
 - [Verilog Implementation](#verilog-implementation)
 - [FPGA Implementation](#fpga-implementation)
 - [Acknowledgement](#acknowledgement)
 - [References](#references)


## Abstract



# Multisim Implementation

Multisim Circuit

Binary inputs:

![image](https://user-images.githubusercontent.com/70422874/182291785-a9d9f56c-1091-48b5-9086-ae162d40021e.png)

BCD inputs:

![image](https://user-images.githubusercontent.com/70422874/182291944-fc0e3a9e-54ac-4679-b202-8aed95b10387.png)


Note: 


# Verilog Implementation

Output for binary inputs:

![image](https://user-images.githubusercontent.com/70422874/182293281-85aabc90-bb9d-4641-b312-356416b8eeb3.png)



Output for BCD inputs:

![image](https://user-images.githubusercontent.com/70422874/182293112-eac72819-2fb7-4cc9-9b03-e1341a3ca54c.png)

# FPGA Implementation

Output for binary inputs:

https://drive.google.com/file/d/16jimVVlwYk-NgNr5mMRVnCYDi5Usp38o/view?usp=sharing

https://drive.google.com/file/d/16gaNhwVHKUTcj0kwB3z5ycAhO7IN5QE4/view?usp=sharing

Output for BCD inputs:

https://drive.google.com/file/d/16buGldU-W6CmDs35bwuphc29KhYQ9aqB/view?usp=sharing

NOTE - Check the blinking of the LEDs, the fast one represents the signal with input frequency, while the slower one represents the frequency divided output signal.

# Acknowledgement
1. Mr. Sayantan Mukherjee, ER(Accys), HAL, Barrackpore Division

# References
[1] Digital Logic And Computer Design By M. Morris Mano.

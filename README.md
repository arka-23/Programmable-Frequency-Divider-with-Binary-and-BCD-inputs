# Design for a Programmable Frequency Divider (50 % duty cycle) with Binary and BCD inputs (with FPGA implementation)
This repository contains the design and simulation of a Programmable Frequency Divider circuit with 50 % duty cycle. [Separate circuits for Binary and BCD inputs] 

# Table of Contents
 - [Abstract](#abstract) 
 - [Multisim Implementation](#multisim-implementation)
 - [Verilog Implementation](#verilog-implementation)
 - [FPGA Implementation](#fpga-implementation)
 - [Acknowledgement](#acknowledgement)
 - [References](#references)


## Abstract

The design and simulation of a programmable frequency divider (50 % duty cycle) is provided  using 
- Asynchronous decade down counter and 
- Asynchronous binary down counter 

by cascading modified MC 4316_new and MC 4318_new (4 bit) IC circuits designed as hierarchical blocks in Multisim, which is fully functional with proper outputs.
The above design which gives a 50% duty cycle when used as frequency divider circuit, has been coded using Verilog
HDL, and the circuit implemented on a Nexus 4 - Arctix 7 FPGA board to verify results.


# Multisim Implementation

Multisim Circuit 

Binary inputs:

![image](https://user-images.githubusercontent.com/70422874/183562775-82614197-c803-4865-88e1-6a31e57628dd.png)

BCD inputs:

![image](https://user-images.githubusercontent.com/70422874/183562198-0872bb1f-cd91-4035-91ad-395e9ffbd926.png)


Note: 


# Verilog Implementation

Schematic for binary inputs:




Schematic for BCD inputs:

Main Design -

![WhatsApp Image 2022-08-09 at 10 52 04 AM](https://user-images.githubusercontent.com/70422874/183571529-3ac209f7-faf1-4ccc-868d-6e08b34160cb.jpeg)

Various internal modules - 

- 7 segment Display

![WhatsApp Image 2022-08-09 at 10 53 46 AM](https://user-images.githubusercontent.com/70422874/183571870-8498ca9a-861a-4a3a-9f08-2bef46b505bb.jpeg)

- Frequency divider output circuit

![WhatsApp Image 2022-08-09 at 11 11 44 AM](https://user-images.githubusercontent.com/70422874/183573937-7756119a-b7b3-483c-b7e3-85be46dd376a.jpeg)

![WhatsApp Image 2022-08-09 at 10 54 26 AM](https://user-images.githubusercontent.com/70422874/183572099-35505b42-382c-41dc-a3f0-277bc1f3e1a3.jpeg)

- 8 bit programmable decade counter (cascaded structure)

![WhatsApp Image 2022-08-09 at 10 55 41 AM](https://user-images.githubusercontent.com/70422874/183572109-175d28be-7427-4aa9-b4c6-574fa2a311ef.jpeg)

- MC 4316_new design 

![WhatsApp Image 2022-08-09 at 10 55 58 AM](https://user-images.githubusercontent.com/70422874/183572129-e085b389-b2ea-4a12-8e48-7cb23d6147d4.jpeg)






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

# Programmable-Frequency-Divider-with-Binary-and-BCD-inputs
This repository contains the design and simulation of a programmable frequency divider (50 % duty cycle)  using 
- Asynchronous decade down counter and 
- Asynchronous binary down counter 

by cascading modified MC 4316 and MC 4318 (4 bit) IC circuits designed as hierarchical blocks, which is fully functional with proper outputs.

Extended work:
◦ The above design is modified to give a 50% duty cycle when used as frequency divider circuit, coded using Verilog
HDL, and the counter circuit is simulated on a Basys 3 - Arctix 7 FPGA board to verify results.

# Table of Contents
   * [Abstract](#abstract)
  * [Block diagram for the proposed model of the digital lock](#block-diagram-for-the-proposed-model-of-the-digital-lock)
  * [Equipment Required](#equipment-required)  
- [Building blocks of the circuit](#building-blocks-of-the-circuit)
  * [Inputs](#inputs)
  * [The Valid Input Detector](#the-valid-input-detector)
  * [The Encoder Circuit](#the-encoder-circuit)
  * [The Counter Circuit](#the-counter-circuit)  
  * [The Three Bit SIPO Register With Counter Acknowledge](#the-three-bit-sipo-register-with-counter-acknowledge)
  * [The Comparator Circuit](#the-comparator-circuit)
  * [The Seven Segment Display](#the-seven-segment-display)
  
 - [Examples to illustrate the working of the circuit](#examples-to-illustrate-the-working-of-the-circuit)
 - [Multisim Implementation](#multisim-implementation)
 - [Verilog Implementation](#verilog-implementation)
 - [Precautions in circuit design](#precautions-in-circuit-design)
 - [Proposed alternate approach](#proposed-alternate-approach)
 - [Contributors](#contributors)
 - [Acknowledgement](#acknowledgement)
 - [References](#references)


## Abstract



## Block diagram for the proposed model of the digital lock:

![AkanshaMukherjee_001910701094 pptx (10)](https://user-images.githubusercontent.com/66127211/177494027-f5a4f163-99ed-4bb5-906f-33325bff9a71.jpg)

## Equipment required for hardware implementation:
* Breadboard
* Switches (transistor based or otherwise) for inputs
* 2:1 Encoder with enable input
* 3 bit serial in parallel out register (may be designed using 3 D flip-flops as well)
* 3 bit comparator (may be designed using logic gates as well)
* Basic logic gates: AND, OR, XOR, XNOR gates
* D flip-flops (3 for synchronous mod 3 counter) with clear input
* Programmable 7 segment display
* Connecting wires
* Voltage supply
* Ground terminal

# Building blocks of the circuit

Each block of the circuit and its function is discussed below:

## Inputs
![AkanshaMukherjee_001910701094 pptx](https://user-images.githubusercontent.com/66127211/177490045-3ec7cba3-3504-4c8f-9f6f-f8e212ff4478.jpg)

## The Valid Input Detector
![AkanshaMukherjee_001910701094 pptx (1)](https://user-images.githubusercontent.com/66127211/177490187-875c26bf-8ec5-4e4f-b3c6-241393147d64.jpg)

## The Encoder Circuit
![AkanshaMukherjee_001910701094 pptx (2)](https://user-images.githubusercontent.com/66127211/177490457-879ac34b-6bae-4008-82b8-43ba83068514.jpg)


## The Counter Circuit
![AkanshaMukherjee_001910701094 pptx (3)](https://user-images.githubusercontent.com/66127211/177490526-1dc6f386-6b2a-479e-9d12-0d1ad0dc3d52.jpg)


## The Three Bit SIPO Register With Counter Acknowledge
![AkanshaMukherjee_001910701094 pptx (4)](https://user-images.githubusercontent.com/66127211/177490819-1a830042-4f05-4f22-ba83-bcfbce55a476.jpg)


## The Comparator Circuit
![AkanshaMukherjee_001910701094 pptx (5)](https://user-images.githubusercontent.com/66127211/177490942-7a29e84f-bd44-44da-b0c9-d90022ad9e0c.jpg)


## The Seven Segment Display
![AkanshaMukherjee_001910701094 pptx](https://user-images.githubusercontent.com/66127211/177491225-ec98351b-fada-4b72-b63c-ac830be26218.jpg)


# Examples to illustrate the working of the circuit

A few sample user inputs are discussed and the signal flow is examined in each case.
![AkanshaMukherjee_001910701094 pptx (3)](https://user-images.githubusercontent.com/66127211/177491476-665c9df6-c43d-4560-bc23-47136ef3e6da.jpg)

![AkanshaMukherjee_001910701094 pptx (2)](https://user-images.githubusercontent.com/66127211/177491532-1203bf2f-d64b-4fe9-b550-923277c89289.jpg)

![AkanshaMukherjee_001910701094 pptx (1)](https://user-images.githubusercontent.com/66127211/177491571-511d94df-ce94-494d-bea4-2a942c1ea07f.jpg)





# Multisim Implementation

Multisim Circuit

![image](https://user-images.githubusercontent.com/70422874/177455847-5807e9d8-2386-46c3-82b2-c29ee50ed69a.png)

Input : 1-2-1 [Matches Key Code - Output Glows]

![image](https://user-images.githubusercontent.com/70422874/177456054-80a648eb-812d-42e7-9242-109c2f0d6ca5.png)

Input : 1-2-2 [Doesnot match Key Code - No Glow]

![image](https://user-images.githubusercontent.com/70422874/177456170-8e72be82-8418-4b14-bf8c-8f0fd02f4c03.png)

Input : 1-2-R

![image](https://user-images.githubusercontent.com/70422874/177456481-fd8f4e9f-fae6-46f0-9a43-3f92a779facd.png)

Note: 

- Red signal - The valid input detector signal
- Green signal - The serial input to the 3 bit SIPO register.


# Verilog Implementation

Verilog Code: For input sequence - 1 2 1

![image](https://user-images.githubusercontent.com/70422874/177451271-d764ad68-54f7-436d-ac1b-5cb289115dfd.png)

![image](https://user-images.githubusercontent.com/70422874/177451329-7f34a398-6890-4210-865e-5a7a3321b928.png)

![image](https://user-images.githubusercontent.com/70422874/177451512-5c686304-cc3a-4fb8-8460-8e34db42167e.png)


Testbench:

![image](https://user-images.githubusercontent.com/70422874/177384405-2edc6433-8922-4d33-ad64-d6f7a69254b9.png)

Output:

![image](https://user-images.githubusercontent.com/70422874/177452458-9295ec87-9fe7-4b5e-ae7f-2a82bf636cbc.png)


Verilog Code: For input sequence - 1 2 2

Testbench:

![image](https://user-images.githubusercontent.com/70422874/177452127-c8bcbdf6-08e1-4167-8eac-1dada5e5eef7.png)

Output:

![image](https://user-images.githubusercontent.com/70422874/177452055-e97efd45-bb94-4bd7-97e0-5d712f6fe9d2.png)

Note:

- lock-> Key Sequence (to be matched with input)
- count-> Counter Outputs
- w3 -> Serial Input Signal
- Q -> SIPO Register Parallel Outputs
- rst -> Reset Signal
- q -> Output Signal


# Precautions in circuit design


# Proposed alternate approach:



# Contributors:
1. Akansha Mukherjee - mukherjeeakansha07@gmail.com
2. Arka Chakraborty - arkachakraborty16@gmail.com

# Acknowledgement
1. Prof. Subir Kumar Sarkar, department of Electronics and Telecommunication, Jadavpur University, Kolkata

# References
[1] Digital Logic And Computer Design By M. Morris Mano.

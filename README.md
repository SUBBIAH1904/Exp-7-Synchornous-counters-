# Exp-6-Synchornous-counters - up counter and down counter 
### AIM: To implement 4 bit up and down counters and validate  functionality.
### HARDWARE REQUIRED:  – PC, Cyclone II , USB flasher
### SOFTWARE REQUIRED:   Quartus prime
### THEORY 

## UP COUNTER 
The counter is a digital sequential circuit and here it is a 4 bit counter, which simply means it can count from 0 to 15 and vice versa based upon the direction of counting (up/down). 

The counter (“count“) value will be evaluated at every positive (rising) edge of the clock (“clk“) cycle.
The Counter will be set to Zero when “reset” input is at logic high.
The counter will be loaded with “data” input when the “load” signal is at logic high. Otherwise, it will count up or down.
The counter will count up when the “up_down” signal is logic high, otherwise count down

Since we know that binary count sequences follow a pattern of octave (factor of 2) frequency division, and that J-K flip-flop multivibrators set up for the “toggle” mode are capable of performing this type of frequency division, we can envision a circuit made up of several J-K flip-flops, cascaded to produce four bits of output.
The main problem facing us is to determine how to connect these flip-flops together so that they toggle at the right times to produce the proper binary sequence.
Examine the following binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1:
Binary count sequence, paying attention to patterns preceding the “toggling” of a bit between 0 and 1.

Note that each bit in this four-bit sequence toggles when the bit before it (the bit having a lesser significance, or place-weight), toggles in a particular direction: from 1 to 0.



 
 

Starting with four J-K flip-flops connected in such a way to always be in the “toggle” mode, we need to determine how to connect the clock inputs in such a way so that each succeeding bit toggles when the bit before it transitions from 1 to 0.

The Q outputs of each flip-flop will serve as the respective binary bits of the final, four-bit count:

Four-bit “Up” Counter
![image](https://user-images.githubusercontent.com/36288975/169644758-b2f4339d-9532-40c5-af40-8f4f8c942e2c.png)



## DOWN COUNTER 

As well as counting “up” from zero and increasing or incrementing to some preset value, it is sometimes necessary to count “down” from a predetermined value to zero allowing us to produce an output that activates when the zero count or some other pre-set value is reached.

This type of counter is normally referred to as a Down Counter, (CTD). In a binary or BCD down counter, the count decreases by one for each external clock pulse from some preset value. Special dual purpose IC’s such as the TTL 74LS193 or CMOS CD4510 are 4-bit binary Up or Down counters which have an additional input pin to select either the up or down count mode.
![image](https://user-images.githubusercontent.com/36288975/169644844-1a14e123-7228-4ed8-81a9-eb937dff4ac8.png)


4-bit Count Down Counter
### Procedure
/* write all the steps invloved */

### PROGRAM 

### Down Counter Code

![ex6 dc code](https://github.com/SUBBIAH1904/Exp-7-Synchornous-counters-/assets/147473604/5a4b4cc2-804e-4365-8dd3-7e52328918f8)

### UP Counter Code

![ex6 uc code](https://github.com/SUBBIAH1904/Exp-7-Synchornous-counters-/assets/147473604/ff109cbe-9d40-4a5b-ae44-5aee2084b0c9)

/*
Program for flipflops  and verify its truth table in quartus using Verilog programming.

Developed by: SUBBIAH S

RegisterNumber: 23005732

*/

### RTL LOGIC UP COUNTER 

![ex6 UC rtl](https://github.com/SUBBIAH1904/Exp-7-Synchornous-counters-/assets/147473604/fc21f8ee-a3ce-49c9-a936-5792aca58dd8)

### RTL LOGIC DOWN COUNTER  

![ex6 DC RTL](https://github.com/SUBBIAH1904/Exp-7-Synchornous-counters-/assets/147473604/f14bb8de-4e3e-4d49-9849-7e1bcddcc660)

### TIMING DIGRAMS UP COUNTER  

![ex6 uc wave](https://github.com/SUBBIAH1904/Exp-7-Synchornous-counters-/assets/147473604/615e884c-7462-4e6d-a5ea-c50165aa7315)

### TIMING DIGRAMS DOWN COUNTER  

![ex6 dc wave](https://github.com/SUBBIAH1904/Exp-7-Synchornous-counters-/assets/147473604/563e657b-2b2c-4737-b7de-711f45b76447)

### RESULTS 

### TRUTH TABLE DOWN COUNTER

![dc truth](https://github.com/SUBBIAH1904/Exp-7-Synchornous-counters-/assets/147473604/4ea0b3fb-3d2c-4a8c-83e5-03dec641d45b)

### TRUTH TABLE UP COUNTER

![UC truth](https://github.com/SUBBIAH1904/Exp-7-Synchornous-counters-/assets/147473604/a5e0610b-c328-47b7-8c6d-e48e734407db)

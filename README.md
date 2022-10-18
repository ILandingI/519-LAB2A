# 519-LAB2A
```   
 Muyuan sheng
 Email:shmuyuan@seas.upenn.edu
 Tested on: Legion Y9000 (i7), windows 11    

```  
## 3.2
* Why is bit-banging impractical on your laptop, despite it having a much faster processor than the RP2040?   
    The computer has many other processes running; if the processor is interrupted will have lots of communication errors.
* What are some cases where directly using the GPIO might be a better choice than using the PIO hardware?  
    GPIOs are better suited for less complex tasks such as input and output, I2C or SPI data lines, outputting PWM waveforms, etc.
* How do you get data into a PIO state machine?  
    Pull instruction takes a data item from the transmit FIFO buffer and places it in the output shift register.
* How do you get data out of a PIO state machine?  
   OSR uses the out instruction to shift this data out.
* How do you program a PIO state machine?  
   We can create a .pio file using C to set up the PIO state machine.
* In the example, which low-level C SDK function is directly responsible for telling the PIO to set the LED to a new color? How is this function accessed from the main “application” code?  
   "pio_sm_put_blocking", Write data to the TX FIFO queue. Block the TX FIFO queue if it is full.  
* What role does the pioasm “assembler” play in the example, and how does this interact with CMake?  
    To compile assembly code into a human-readable format. 
 ## 3.3
Please check the [ws2812.c](https://github.com/ILandingI/519-LAB2A/blob/c793b1927cb640dd79a0c067819594c2086ef04e/annotated_ws2812.c) and .h

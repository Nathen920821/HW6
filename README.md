# HW6  
For hw6-1.cpp and hw6-2.cpp you can replace the main.cpp in the mbed-os-empty example project. Then, it can be compiled and run on the stm32 iot node development board via Mbed Studio.  

For hw6-3.cpp refer to https://github.com/janjongboom/b-l475e-iot01a-audio-mbed  

hw6-2 setups DMA to transfer the data from ADC data register to a specific buffer when each conversion finishes. When the top half of buffer is filled, the interrupt will be generated and print all data in the top half of buffer. When the bottom half of buffer is filled, the interrupt makes all data in the bottom half of buffer printed.   

hw6-3 setups DMA to transfer audio data to PCM_Buffer. When the top and bottom half of PCM_Buffer are filled, the corresponding interrupts will generate. We choose two GPIO pins D4, D5 as output and connect them to logic analyzer. Once the PCM_Buffer top half event occurs, toggle pin1’s output voltage. Once the PCM_Buffer bottom half event occurs, toggle pin2’s output voltage. By this way, we can observe the frequency of audio sampling.

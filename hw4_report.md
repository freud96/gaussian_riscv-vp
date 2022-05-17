Written by Freud L. Lewis Piercius, student ID: 110061422

Homework 4 report

**Introduction**
    RISC-V is a free and open Instruction Set Architecture that is based on established reduced instruction set computer principles. For this homework, we are supposed to use the Virtual Prototype to to control hardware modules through bus. In this homework, we port the Gaussian blur module to the VP.
    
    
    
 **Implementation**
    The algorithm for the Gaussian filter is kept same as previous Homework. To implement the platform, we use the basic platform provided by RISC-V. the gaussian filter module is declared as "SobelFilter.h", reason is we simply used the same platform as in lab8 by modifying the header file itself and filter_def.h(replacing the kernel). In the main.cpp of the platform, just as in lab8, we keep the same addresses, the same number of sockets on the bus. The software code will read the bmp file, send neighboring pixels to the hardware module to then retrieve the result after processing.  
 
 
**Experiment and result**
    For this homework, we focus on the difference by using DMA shown in https://github.com/freud96/gaussian_riscv-vp/blob/main/DMA_transfer_code.png  for performing transfer between from/to Sobel filter module or using processor(memcpy) shown in https://github.com/freud96/gaussian_riscv-vp/blob/main/Processor_move.JPG. when we only use processor, it took approximitely **3431411650 ns** to simulate while for when using DMA it took only  **3208588470 ns**. Then number of instruction executed with DMA moving is far less **73926408** than using processor **86378263**. Result of DMA simulation can be found at https://github.com/freud96/gaussian_riscv-vp/blob/main/DMA.JPG and Result of processor transfering data at (link). The reason why the simulated time and instruction number is lesser when using DMA is that the accelerator accesses the main memory without the processor unit. 


    





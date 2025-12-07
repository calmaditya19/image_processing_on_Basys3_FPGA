# image_processing_on_Basys3_FPGA
IvLabs project to create a module to apply multiple filters simultaneously on a given image and display it on monitor via VGA

This project uses **Verilog** to implement a hardware-accelerated **Image Processing system on a Basys 3 FPGA**.  It stores the frame in the FPGA's on-chip **Block RAM (BRAM)** after receiving **QVGA (320x240) RGB444** image data from a computer via **UART**.

 A **VGA Controller** for displaying the image on a **640x480 monitor** and a **Convolution** module for applying filters such as blurring are part of the core RTL design.  Neighboring pixels are made available for real-time convolution operations by a sequence of **LineBuffers**.

 The system can switch between **Display Mode** (for continuous viewing and filtering) and **Receive Mode** (for data upload) using a physical switch.  The design makes use of **AMD Vivado** and **Python (OpenCV/PySerial)** for data transmission and image resizing.

 For further information visit
  ![HackMD]([Target URL](https://hackmd.io/@Ash-Fpga/SJgLLpiOe-l))

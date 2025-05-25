# Conv_on_PYNQ
## Project Overview
This project demonstrates how to load a custom convolution hardware IP onto a PYNQ FPGA board, transfer data between the Processing System (PS) and Programmable Logic (PL) using CDMA, and verify the output against a golden reference using Python and the PYNQ framework.
## System setup
* **Platform**: pynq-z2
* **Files**:
  * `input.hex` - Input data in hexdecimal format
  * `golden.hex` - Expected output data for verfication

## Hardware Configuration
The design includes:

* **AXI CDMA**: for memory-to-memory data transfer
* **AXI GPIO**: to start the custom IP
* **Custom Convolution IP**: mapped to PL fabric

Address map:

| Component |	Address |
|-----------|---------|
| Zynq DDR Memory |	0x30000000 |
| BRAM0 (input) |	0xC0000000 |
| BRAM1 (output) |	0xC2000000 |
| AXI CDMA | from IP dictionary |
| AXI GPIO |from IP dictionary | 

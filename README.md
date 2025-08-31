# SGW — Automotive Gateway Device

This project describes custom software for a **Secure Gateway (SGW)** device designed for automotive networking applications.  
It is based on a powerful MCU and multiple high-speed CAN transceivers that ensure reliable in-vehicle communication.

---

## Hardware Overview

### MCU: **SPC58** 100TQFP (STMicroelectronics)  
The **SPC58 series** are automotive microcontrollers based on Power Architecture®, designed for safety-critical applications:

##### **JTAG** 
- VDD
- 60 PIN TDI
- 61 PIN TMS
- 62 PIN TDO
- 64 PIN TCK
- 63 PIN NTRST_PD

---

### CAN Transceivers: **TJA1044** and **TJA1046** (NXP)

#### **TJA1044** (×2)  
High-speed CAN transceiver (Mantis family), providing the physical link between a CAN controller and the bus:  

##### **First** TJA1044
- 1 PIN TXD -> MCU PIN79
- 4 PIN RXD -> MCU PIN80
- 7 PIN CANH -> connector PIN5 /12
- 6 PIN CANL -> connector PIN12/12

##### **Second** TJA1044
- 1 PIN TXD -> MCU PIN82
- 4 PIN RXD -> MCU PIN83
- 7 PIN CANH -> connector PIN1/8
- 6 PIN CANL -> connector PIN6/8

---

#### **TJA1046** (×3)  
Dual high-speed CAN transceiver, essentially integrating two TJA1044GT transceivers in a compact package:  

##### **First** TJA1046
- 1 PIN TXD1 -> MCU PIN70
- 4 PIN RXD1 -> MCU PIN71
- 5 PIN TXD2 -> MCU PIN72
- 8 PIN RXD2 -> MCU PIN73
- 13 PIN CANH1 -> connector PIN1/12
- 12 PIN CANL1 -> connector PIN8/12
- 10 PIN CANH2 -> connector PIN2/12
- 9  PIN CANL2 -> connector PIN9/12

##### **Second** TJA1046
- 1 PIN TXD1 -> MCU PIN74
- 4 PIN RXD1 -> MCU PIN75
- 5 PIN TXD2 -> MCU PIN77
- 8 PIN RXD2 -> MCU PIN78
- 13 PIN CANH1 -> connector PIN3 /12
- 12 PIN CANL1 -> connector PIN10/12
- 10 PIN CANH2 -> connector PIN4 /12
- 9  PIN CANL2 -> connector PIN11/12

##### **Third** TJA1046
- 1 PIN TXD1 -> MCU PIN84
- 4 PIN RXD1 -> MCU PIN85
- 5 PIN TXD2 -> MCU PIN99
- 8 PIN RXD2 -> MCU PIN100
- 13 PIN CANH1 -> connector PIN2/8
- 12 PIN CANL1 -> connector PIN7/8
- 10 PIN CANH2 -> connector PIN3/8
- 9  PIN CANL2 -> connector PIN8/8

---

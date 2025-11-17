# LED-BLINK
# 💡 Experiment 01 – Interfacing a Digital Output (LED) with ARM Development Board

### 🎯 **Aim**
To interface a digital output (LED) to an ARM development board and write a blink code.

---

### ⚙️ **Components Required**
- STM32CubeIDE  
- NUCLEO ARM Development Board  

---

### 🧠 **Theory**

**ARM (Advanced RISC Machine)** is a 32-bit processor architecture developed by ARM Holdings. It is widely used in embedded systems and SoC (System-on-Chip) products. Many semiconductor companies like Samsung, Atmel, and Texas Instruments license ARM architecture to design their own SoCs.
### 🧩 **What is an ARM7 Processor?**
The **ARM7 processor** is commonly used in embedded system applications. It provides a balance between the classic ARM architecture and the newer Cortex series, offering an excellent platform for both hardware and software development.
### 🔍 **LPC2148 Microcontroller**
The **LPC2148**, developed by NXP Semiconductors (Philips), is a 16/32-bit ARM7-based microcontroller featuring a wide range of peripherals.
#### **Key Features**
- 16/32-bit ARM7TDMI-S core in LQFP64 package  
- On-chip **Flash memory**: 32 KB – 512 KB  
- On-chip **SRAM**: 8 KB – 40 KB  
- **ISP/IAP** via on-chip bootloader  
- **Embedded ICE-RT** and **Real Monitor** for real-time debugging  
- **USB 2.0** full-speed device controller with 2 KB endpoint RAM  
- **10-bit ADC** (6 or 14 channels, 2.44 μs conversion time)  
- **10-bit DAC** for analog output  
- **Timers:** Two 32-bit timers, watchdog, and PWM unit  
- **RTC** with 32 kHz clock input  
- **UARTs (2x), I²C (2x)** up to 400 kbit/s  
- **5V-tolerant GPIOs**, 21 external interrupt pins  
- **Max CPU Clock:** 60 MHz using on-chip PLL (lock time 100 µs)  
- **Crystal Frequency:** 1 MHz – 25 MHz  
- **Power modes:** Idle and Power-down with peripheral clock scaling  

---

### 🧭 **Procedure**

1.<img width="1920" height="1080" alt="Screenshot 2025-11-16 174343" src="https://github.com/user-attachments/assets/710abe9f-bf5b-424d-9794-dfd76665abe7" />

2.<img width="1920" height="1080" alt="Screenshot 2025-11-17 084712" src="https://github.com/user-attachments/assets/7be403d2-f04f-4e20-ab1b-07d490d10870" />

3.<img width="1920" height="1080" alt="Screenshot 2025-11-17 083659" src="https://github.com/user-attachments/assets/ddad4e43-2888-4687-9995-b93ce795ddd1" />

4.<img width="1920" height="1080" alt="Screenshot 2025-11-17 083727" src="https://github.com/user-attachments/assets/469b0b8b-836f-4be8-9a0f-d043ec294acc" />

5.<img width="1920" height="1080" alt="Screenshot 2025-11-17 083858" src="https://github.com/user-attachments/assets/d2b12017-b19d-4f21-aef8-51a002495dc8" />

6.<img width="1920" height="1080" alt="Screenshot 2025-11-17 083803" src="https://github.com/user-attachments/assets/8d04f6ba-0bdf-492a-bc7b-5c3d83504c57" />

7.<img width="1920" height="1080" alt="Screenshot 2025-11-17 084047" src="https://github.com/user-attachments/assets/beb9cccb-6213-476d-9482-cc3b414a4f7d" />

8.<img width="1920" height="1080" alt="Screenshot 2025-11-17 084129" src="https://github.com/user-attachments/assets/108380b2-f0c1-4cd2-a43c-d2762e9c6575" />

9.<img width="1920" height="1080" alt="Screenshot 2025-11-17 084224" src="https://github.com/user-attachments/assets/a3e65a3b-4463-4c29-bbe1-c9485b152f3e" />


### 💻 **Program**


```
#include "main.h"

void SystemClock_Config(void);
static void MX_GPIO_Init(void);

int main(void)
{
    HAL_Init();
    SystemClock_Config();
    MX_GPIO_Init();

    while (1)
    {
        HAL_GPIO_WritePin(GPIOA, GPIO_PIN_5, GPIO_PIN_RESET);
        HAL_Delay(1000);
        HAL_GPIO_WritePin(GPIOA, GPIO_PIN_5, GPIO_PIN_SET);
        HAL_Delay(1000);
    }
}
```
---
### OUTPUT
CASE 1: LED ON 
<img width="1392" height="624" alt="Screenshot 2025-11-17 084326" src="https://github.com/user-attachments/assets/0666261a-d219-4ce8-b898-b244f3b5808c" />

CASE 2: LED OFF
<img width="1392" height="622" alt="Screenshot 2025-11-17 084342" src="https://github.com/user-attachments/assets/f8d56017-4381-49ea-a773-7b4e05ff8cf5" />

---
### RESULT
Interfacing a digital output with ARM microcontroller is executed and the results are verified.

# # Day 1 – Introduction to Embedded Systems
##  What is an Embedded System?
An **Embedded System** is a microcontroller-based **hardware + software** system designed to perform **a specific function**.
software that running by the hardware is known as Firmware.
 ## Real-Life Examples for microcontroller:   ## Examples for microprocessor      ##Examples for soc's(System on chip)
- Washing Machine                              -CT Scanner                         -Tv Remote
- micro oven                                    Drones                             -SmartPhone
- Air purifiers                                 Pc's,laptops                       -Surveilance Camera
- Ac's                                          Servers
  Microprocessor,Microcontroller,Soc's they execute instructions(Machinelevel/Lowlevel)
## 🔹 What is a Microcontroller?
A **Microcontroller** is a compact integrated circuit that contains:
- CPU
- RAM
- ROM
- Timers
- I/O Ports
**It is used in embedded systems.**
### 🔸 Examples:
- 8051 Microcontroller
- ATmega328 (Arduino)
- PIC Microcontroller
- ARM Cortex-M series

## 🔹 What is a Microprocessor?
A **Microprocessor** is just the **CPU** (Central Processing Unit).  
It needs external memory, input/output, and timers.
It is used in general-purpose systems (like computers, laptops).
### 🔸 Examples:
- Intel 8085
- Intel i3, i5, i7
- AMD Ryzen 5
## 🔹 What is SoC (System on Chip)?
A **System on Chip (SoC)** is an **entire computer system on a single chip**, including:
- Processor
- Memory
- Peripherals
- Graphics
- Wireless communication (like Wi-Fi, Bluetooth)
Soc's is designed by combining some of the best features of microcontroller and some of the best features of microprocessor.
### 🔸 Examples:
- Qualcomm Snapdragon (in phones)
- Apple M1 Chip
- Raspberry Pi (uses SoC)
## 🔹 Difference Between Microcontroller and Microprocessor

|  Feature              |  Microcontroller                            | Microprocessor                         |
|------------------------|----------------------------------------------|------------------------------------------|
| Components             | CPU + RAM + ROM + I/O in one chip            | Only CPU (others are external)           |
| Memory                 | Less (built-in)                              | More (external RAM, storage)             |
| Operating System       | Usually no OS / small RTOS                   | Can run full OS (Windows/Linux)          |
| Speed                  | Slower                                       | Faster                                   |
| Power Consumption      | Low                                          | High                                     |
| Cost                   | Low                                          | High                                     |
| Applications           | Washing machine, Microwave, TV remote       | PC, Laptop, Game console                 |
| Best Feature           | All components integrated in one chip       | High performance & multitasking          |
| Used in                | Embedded systems                             | General-purpose systems                  |

## ✅ Summary:
- **Embedded System**: A specific-purpose mini-computer built around a microcontroller.
- **Microcontroller**: All-in-one chip for small embedded applications.
- **Microprocessor**: Only CPU; needs external parts.
- **SoC**: Entire computer system on a single chip.

  

## Day 2 – System on Chip (SoC)
##  Definition:
A **System on Chip (SoC)** is an integrated chip that combines all the essential components of a computer system on a **single chip**.
It includes:
- CPU (like in microprocessors)
- Memory (RAM, ROM)
- I/O Ports (like in microcontrollers)
- Peripherals (Wi-Fi, Bluetooth, Timers, ADC, etc.)
 SoC is a **combination of the best features** of both **Microcontroller** and **Microprocessor**:
- Like a **Microcontroller**: It has all components integrated into one chip
- Like a **Microprocessor**: It supports high performance and multitasking
# IDEs Used for Microcontroller Programming
 What is an IDE?
**IDE** stands for **Integrated Development Environment**.  
It is a software that contains all the tools required to develop embedded software in one place.
## 🔹 Tools Included in an IDE:
1. **Text Editor** – for writing code  
2. **Compiler** – to convert code into machine language  
3. **Debugger** – to find and fix errors  
4. **Loader / Linker** – to combine files and prepare output
## 🔹 Popular IDEs for Microcontroller:
### 1. **Arduino IDE**
- Used for Arduino boards (UNO, Nano, Mega, etc.)
- Beginner-friendly
- Generates `.hex` files after compilation
- Easy uploading via USB

### 2. **Keil µVision IDE**
- Used for 8051, ARM, and STM32 microcontrollers
- Used in professional and industrial environments
- Supports debugging, simulation, and memory configuration
- Generates `.hex` files for flashing into microcontrollers
## 🔹 What is a Hex File?
Once your embedded C program is compiled, it generates a **`.hex` file**, which is the actual machine code that is loaded into the microcontroller.

# Microprocessor
Microprocessor can not uses the arduino and keil.It will uses the full fledged os(Macos,Windows,linux)

# Soc's
Soc also uses full fledged os i.e.,EmbeddedLinux(or)Variants of linux
Example--Smart phone -android linux
         Samsung smart tvs-TizenosLinux
         LG -Webos Linux
         Router -Openwrt(Open wireless router)linux

## Day3 Development tools
1.Text Editor: C program is written by using text editor
2.Compiler- converts c statemnets into instruction
Instructions contains Opcode and operands

 





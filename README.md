# RK3588-Edge-AI-Gateway-PCB-Case-Study
Self-Employed / Freelance

<img width="1130" height="832" alt="Image" src="https://github.com/user-attachments/assets/b94b2a72-d357-4c82-b7c0-07d8c0e88979" />

This repository presents a public hardware design case study for an RK3588-based Edge AI Gateway PCB. The platform is based on a dual-processor architecture using Rockchip RK3588 as the primary AI/application processor and TI AM6442 as a networking, USB, and storage co-processor. The system targets edge-computing applications such as industrial automation, intelligent video processing, robotics, and real-time networking.

The design includes onboard 32 GB LPDDR4 memory using 2× Micron MT53E4G32D8GS-046_AIT:C devices, PCIe-based communication, MIPI CSI/DSI camera and display interfaces, dual Gigabit Ethernet, USB 3.0/USB 2.0, microSD/eMMC storage paths, USB-C PD power input, 12V barrel input, and a SEAF-20 gateway-card expansion connector.

My work focused on translating the system-level hardware requirements into schematic architecture, high-density PCB layout planning, power distribution, memory integration, high-speed interface routing strategy, and manufacturable hardware documentation.


## My Role

- Converted system-level hardware requirements into schematic architecture and PCB design planning.
- Worked on high-density PCB layout strategy for RK3588, AM6442, onboard LPDDR4 memory, storage, USB, Ethernet, and expansion interfaces.
- Planned routing constraints for high-speed interfaces including PCIe, MIPI CSI/DSI, USB, RGMII, and memory signals.
- Worked on multi-rail power distribution, USB-C PD input architecture, and board-level power planning.
- Prepared documentation, component-level planning, and manufacturable design outputs for hardware review.


## Key Design Features

- Rockchip RK3588 primary AI/application processor
- TI AM6442 networking and real-time co-processor
- Onboard 32 GB LPDDR4 memory using 2× MT53E4G32D8GS-046_AIT:C
- PCIe-based inter-processor communication
- MIPI CSI camera interface
- MIPI DSI display interface
- Dual Gigabit Ethernet using KSZ9031 PHYs
- USB 3.0 host/debug interface
- AM6442 USB 2.0 high-speed interface
- microSD/eMMC storage architecture
- USB-C PD power input and 12V barrel input
- Power-path OR/mux control
- Multi-rail power architecture
- SEAF-20 gateway-card expansion interface


## Memory Architecture

The design uses onboard LPDDR4 memory instead of removable memory connectors. The memory subsystem is built around 2× Micron MT53E4G32D8GS-046_AIT:C LPDDR4 devices.

### Memory Device

- Part Number: MT53E4G32D8GS-046_AIT:C
- Manufacturer: Micron
- Type: LPDDR4
- Density: 128 Gbit per device
- Organization: 4G × 32
- Bus Width: x32
- Speed: 4266 MT/s
- Operating Temperature: -40°C to +95°C
- Total Memory Used: 2 devices × 128 Gbit = 256 Gbit = 32 GB

This onboard memory approach reduces mechanical connector dependency and supports a compact high-density PCB design, but increases routing complexity, placement sensitivity, and memory-layout constraints.

## Interface Summary

### RK3588 Interfaces
- LPDDR4 memory
- PCIe 3.0 x4 for gateway-card interface
- PCIe link for inter-processor communication
- MIPI CSI camera interface
- MIPI DSI display interface
- USB 3.0 host/debug
- microSD boot/storage
- I2C, GPIO, UART, reset, and control signals

### AM6442 Interfaces
- Dual RGMII Gigabit Ethernet
- USB 2.0 high-speed OTG-capable interface
- eMMC storage
- microSD boot/config/logging
- UART, I2C, reset, and control signals

### Expansion / Gateway Interface
- SEAF-20 120-pin connector
- PCIe x4
- Power rails
- Clocks
- JTAG
- UART
- I2C
- GPIO
- RF control signals


## Power Architecture

The board uses a multi-rail power architecture supporting RK3588, AM6442, memory, storage, USB, Ethernet PHYs, camera/display interfaces, and the gateway expansion connector.

The input architecture supports:
- 12V barrel jack input
- USB-C Power Delivery input
- Power-path OR/mux control
- Protected and sequenced system rails

Main power domains include:
- RK3588 core and I/O rails
- AM6442 core and I/O rails
- LPDDR4 memory rails
- 5V USB/peripheral rail
- 3.3V system logic rail
- 1.8V I/O/storage rail
- Ethernet PHY rails
- Camera/display rails


<img width="3508" height="3969" alt="Image" src="https://github.com/user-attachments/assets/04e9a361-1c08-45e2-9274-20d06d1fbf07" />



<img width="877" height="992" alt="Image" src="https://github.com/user-attachments/assets/12e9ff9d-8af2-4c8d-a40b-2a4a4a1c8882" />



<img width="767" height="737" alt="Image" src="https://github.com/user-attachments/assets/1fe8666c-e39a-46d6-a796-cc8183f83d89" />



<img width="775" height="740" alt="Image" src="https://github.com/user-attachments/assets/95e2a170-ed8e-4e3d-8400-5d5784d25e27" />



<img width="732" height="741" alt="Image" src="https://github.com/user-attachments/assets/b3df06cb-9b40-49b1-8a93-f46bbe0a16f6" />



<img width="756" height="751" alt="Image" src="https://github.com/user-attachments/assets/d8791d1d-836e-431e-8c93-47f60f6c168d" />



<img width="1190" height="841" alt="Image" src="https://github.com/user-attachments/assets/954bb014-0deb-4083-ae75-9c1882e22ba6" />



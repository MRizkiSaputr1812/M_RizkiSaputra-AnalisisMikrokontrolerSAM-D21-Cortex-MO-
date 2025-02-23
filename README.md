# AnalisisMikrokontrolerSAM-D21-Cortex-MO-

# SAM-D21-Cortex-MO- : Struktur, Spesifikasi, dan Control unit

![image](https://github.com/user-attachments/assets/98d285f8-7df0-4420-b53e-61725e78e859)
(ATSAMD21)

## 1. Penjelasan SAMD21 Cortex-M0+
SAMD21 adalah mikrokontroler berbasis ARM Cortex-M0+ yang diproduksi oleh Microchip Technology (sebelumnya Atmel). Mikrokontroler ini sering digunakan dalam aplikasi IoT, perangkat wearable, dan sistem tertanam karena konsumsi dayanya yang rendah serta performa yang cukup baik.

## 2. Struktur SAMD21 Cortex-M0+
Struktur utama dari SAMD21 terdiri dari beberapa blok utama, yaitu:
1) Core (ARM Cortex-M0+)

- CPU berbasis 32-bit RISC (Reduced Instruction Set Computing)
- Pipeline 2-stage untuk eksekusi instruksi yang efisien
- Mendukung Thumb-2 Instruction Set

2) Memori
- Flash Memory: 32KB hingga 256KB (tergantung model)
- SRAM: 4KB hingga 32KB
- EEPROM (Emulated)

3) Peripheral & Interface
- Timer/Counters: Timer 16-bit & 32-bit
- Communication Interface: I²C, SPI, UART/USART
- USB 2.0 Full Speed dengan fitur OTG (On-The-Go)
- PWM (Pulse Width Modulation)
- ADC (Analog to Digital Converter) 12-bit
- DAC (Digital to Analog Converter) 10-bit

4) Power Management
- Operating Voltage: 1.62V - 3.6V
- Ultra-Low Power Mode: Sleep & Standby
  
5) Interrupt System
- Mendukung NVIC (Nested Vectored Interrupt Controller) dengan hingga 32 interrupt
- Mendukung SysTick Timer untuk scheduling

## 3. Spesifiksi umum SAMD21 Cortex-M0+
- CPU Core ARM Cortex-M0+
- Clock Speed	Hingga 48 MHz
- Flash Memory	32KB - 256KB
- SRAM	4KB - 32KB
- Operating Voltage	1.62V - 3.6V
- I/O Pins	Hingga 38 GPIO
- Communication Interfaces	I²C, SPI, UART, USB 2.0 FS
- Timers	16-bit & 32-bit
- Low Power Modes	Sleep, Standby, Idle

## 4. Control Unit SAMD21
Control unit (CU) dalam SAMD21 mengelola operasi CPU dan mengatur komunikasi antara CPU dan peripheral. Beberapa fitur utama dari control unit adalah:

1) CPU Execution Control
- Mengatur jalannya instruksi dalam pipeline 2-stage
- Mendukung eksekusi instruksi Thumb-2
  
2) Clock & Power Management
- GCLK (Generic Clock Controller): Mengatur sumber clock untuk berbagai peripheral
- Power Management Controller (PM): Mengelola mode daya rendah untuk efisiensi konsumsi daya

3) Interrupt Handling
- NVIC (Nested Vectored Interrupt Controller): Menangani interupsi secara cepat
- Event System (EVSYS): Memungkinkan komunikasi antar peripheral tanpa intervensi CPU

4) Memory & Bus Management
- AHB (Advanced High-performance Bus): Menghubungkan CPU ke memori dan peripheral
- APB (Advanced Peripheral Bus): Menghubungkan peripheral ke AHB untuk efisiensi akses

## 5. Kelebihan dan Kekurangan SAMD21 Cortex-M0+

- Kelebihan
✅ Konsumsi daya rendah → Cocok untuk aplikasi berbasis baterai
✅ Performa cukup baik → Dengan clock hingga 48 MHz
✅ Banyak peripheral → ADC, DAC, USB, PWM, dll.
✅ Mendukung USB 2.0 FS → Bisa digunakan untuk komunikasi USB langsung
✅ Flash & SRAM cukup besar → Bisa menangani aplikasi embedded yang kompleks
✅ Clocking fleksibel → Bisa dikonfigurasi sesuai kebutuhan daya

- Kekurangan
❌ Tidak memiliki FPU (Floating Point Unit) → Kurang optimal untuk komputasi floating point
❌ Clock speed terbatas (48 MHz) → Lebih rendah dibanding Cortex-M3/M4
❌ RAM terbatas (maks 32KB) → Bisa menjadi kendala dalam aplikasi besar
❌ Tidak mendukung debugging yang kompleks → Tidak ada fitur seperti Trace Port Interface


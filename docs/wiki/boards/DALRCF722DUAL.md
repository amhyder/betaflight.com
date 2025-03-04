# DALRCF722DUAL

The DALRCF722DUAL described here:

This board use the STM32F722RET6 microcontroller and have the following features:

- High-performance and DSP with FPU, ARM Cortex-M7 MCU with 512 Kbytes Flash
- 216 MHz CPU,462 DMIPS/2.14 DMIPS/MHz (Dhrystone 2.1) and DSP instructions, Art Accelerator, L1 cache, SDRAM
- DUAL gyro MPU6000 and ICM20602,could choose mpu6000,more stable and smooth.Or choose ICM20602,higher rate(32K/32K).Choose on CLI mode,experience different feature gyro on same board
- OSD on board
- The 16M byte SPI flash on board for data logging
- USB VCP and boot select button on board(for DFU)
- Stable voltage regulation,DUAL BEC 5v/2.5A and 10v/2A for VTX/camera etc.And could select 5v/10v with pad
- Serial LED interface(LED_STRIP)
- VBAT/CURR/RSSI sensors input
- Suppose IRC Tramp/smart audio/FPV Camera Control/FPORT/telemetry
- Supports SBus(built-in inverters), Spektrum1024/2048, PPM
- Supports I2C device extend(baro/compass/OLED etc)(socket)
- Supports GPS (socket)

### All uarts have pad on board

| Value | Identifier | RX   | TX   | Notes                                  |
| ----- | ---------- | ---- | ---- | -------------------------------------- |
| 1     | USART1     | PB7  | PB6  | PB7 FOR SBUS IN(inverter build in)/PPM |
| 2     | USART2     | PA3  | PA2  | PAD USE FOR TRAMP/smart audio          |
| 3     | USART3     | PC11 | PC10 | USE FOR GPS                            |
| 4     | USART4     | PA1  | PA0  | PA0 FOR RSSI/FPORT/TEL etc             |
| 5     | USART5     | PD2  | PC12 | PAD                                    |

### I2C with GPS port together.Use for BARO or compass etc

| Value | Identifier | function | pin | Notes |
| ----- | ---------- | -------- | --- | ----- |
| 1     | I2C1       | SDA      | PB9 |
| 2     | I2C1       | SCL      | PB8 |

### Buzzer/LED output

| Value | Identifier | function | pin  | Notes    |
| ----- | ---------- | -------- | ---- | -------- |
| 1     | LED0       | LED      | PC14 | On board |
| 2     | BEEPER     | BEE      | PC13 | Pad      |

### VBAT input with 1/10 divider ratio,Current signal input,Analog/digit RSSI input

| Value | Identifier | function | pin | Notes |
| ----- | ---------- | -------- | --- | ----- |
| 1     | ADC1       | VBAT     | PC1 |
| 2     | ADC1       | CURR     | PC0 |
| 3     | ADC1       | RSSI     | PA0 |

### 8 Outputs

| Value | Identifier | function | pin  | Notes                    |
| ----- | ---------- | -------- | ---- | ------------------------ |
| 1     | TIM4_CH2   | PPM      | PB7  | PPM                      |
| 2     | TIM8_CH1   | OUPUT1   | PC6  | DMA                      |
| 3     | TIM8_CH2   | OUPUT2   | PC7  | DMA                      |
| 4     | TIM8_CH3   | OUPUT3   | PC8  | DMA                      |
| 5     | TIM8_CH4   | OUPUT4   | PC9  | DMA                      |
| 6     | TIM1_CH1   | OUPUT5   | PA8  | DMA                      |
| 7     | TIM1_CH2   | OUPUT6   | PA9  | DMA                      |
| 8     | TIM1_CH3   | OUPUT7   | PA10 | DMA NO PAD               |
| 9     | TIM2_CH4   | OUPUT8   | PB11 | NO PAD                   |
| 10    | TIM2_CH1   | PWM      | PA15 | DMA LED_STRIP            |
| 11    | TIM3_CH4   | PWM      | PB1  | FPV Camera Control(FCAM) |

### Gyro & ACC ,support ICM20602 and MPU6000

| Value | Identifier | function | pin  | Notes              |
| ----- | ---------- | -------- | ---- | ------------------ |
| 1     | SPI1       | SCK      | PA5  | MPU6000 & ICM20602 |
| 2     | SPI1       | MISO     | PA6  | MPU6000 & ICM20602 |
| 3     | SPI1       | MOSI     | PA7  | MPU6000 & ICM20602 |
| 4     | SPI1       | CS1      | PB0  | MPU6000            |
| 5     | SPI1       | CS2      | PA4  | ICM20602           |
| 6     | SPI1       | INT1     | PB10 | MPU6000            |
| 7     | SPI1       | INT2     | PC4  | ICM20602           |

### OSD MAX7456

| Value | Identifier | function | pin  | Notes |
| ----- | ---------- | -------- | ---- | ----- |
| 1     | SPI2       | SCK      | PB13 |
| 2     | SPI2       | MISO     | PB14 |
| 3     | SPI2       | MOSI     | PB15 |
| 4     | SPI2       | CS       | PB12 |

### 16Mbyte flash

| Value | Identifier | function | pin | Notes |
| ----- | ---------- | -------- | --- | ----- |
| 1     | SPI3       | SCK      | PB3 |
| 2     | SPI3       | MISO     | PB4 |
| 3     | SPI3       | MOSI     | PB4 |
| 4     | SPI3       | CS       | PB2 |

### SWD

| Pin | Function | Notes |
| --- | -------- | ----- |
| 1   | SWCLK    | PAD   |
| 2   | Ground   | PAD   |
| 3   | SWDIO    | PAD   |
| 4   | 3V3      | PAD   |

![DALRCF722DUAL top](images/DALRCF722DUAL-Top.png)
![DALRCF722DUAL bottom](images/DALRCF722DUAL-Botton.jpg)

###Designers

- ZhengNyway(nyway@vip.qq.com)

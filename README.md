# FusionController
#### UART Settings 1200, N, 1
#### Blue Wire: Eye Transmit
**Sample Packet:** 170 4 5 0 0 46 9 100 0 16 3 2 0 0 249

**Byte 0:** Command - always 170 from what I can see

**Byte 1:** Always 4 but not sure what it means

**Byte 2:** Packet sequence number

**Byte 3:** Always 0

**Byte 4:** Always 0

| Byte| Bit 0        |  1          |  2  | 3 | 4 | 5 | 6 | 7 |
|-----| ------------- |-------------| -----|-----|-----|-----|-----|-----|
| 5   |  See Below | See Below  |  |



| Mode | Frame | Byte| Bit 0        |  1          | 
|-----|-----|-----| -------------|-------------|
| P1 | Odd | 5   |  0           | 1           | 
| P1 | Even | 5   |  1           | 1           | 
| P2 | Odd | 5   |  1           | 1           | 
| P2 | Even | 5   |  0           | 0           | 
| P3 | Odd | 5   |  0           | 0           | 
| P3 | Even | 5   |  1           | 0           | 



| Byte| Bit 0        |  1          |  2  | 3 | 4 | 5 | 6 | 7 |
|-----| -------------|-------------| -----|-----|-----|-----|-----|-----|
| 6   |      1 - ? Unknown        |  | P5 - Accelerate/Kick Start | P4 - MPH/KPH |

**Byte 7:** P8 - Max Output 5 - 100%

**Byte 8:** Always 0

**Byte 9:** Usuall 144 but did see 16

**Byte 10:** PA - Electronic Brake 0 Off - 5 Powerful

**Byte 11:** P9 - Battery Save Mode - 1 Max, 2 Mid, 3 None

**Byte 12:** P7 - Acceleration Mode - 0 Powerfull - 5 Slow Start

**Byte 13:** Always 0

**Byte 14:** Checksum8 Xor - Bytes 0 - 12 - https://www.scadacore.com/tools/programming-calculators/online-checksum-calculator/

#### Yellow Wire: Controller Transmit

#### Orange Wire: 65v Unknown - But I think it turns the Scooter on.  It's only on when the scooter is on

#### Green Wire: Throttle Control 0.81 ~ 3.66

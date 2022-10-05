某宝购入的1.44寸SPI接口彩色液晶屏，官方仅提供C语言版本示例。为了便于使用，使用MicroPython将其移植至Raspberry Pi Pico平台。代码中自带英文字库，可以显示ASCII字符。

![商品链接](https://s2.loli.net/2022/10/05/QripF98dHtAPfsM.jpg)

# 引脚接线

| 模块引脚 | 作用          | Raspberry Pi Pico 引脚 |
| -------- | ------------- | ---------------------- |
| VCC      | 电源正极      | GND                    |
| GND      | 电源地        | 3V3(OUT)               |
| SCL      | SPI时钟       | GP2                    |
| SDA      | SPI数据       | GP3                    |
| RES      | 复位          | GP1                    |
| DC       | 数据/命令选择 | GP0                    |
| CS       | SPI片选       | GND                    |
| BL       | 背光控制      | 3V3(OUT)               |

**说明：** CS引脚为SPI片选引脚，如果需要进行从设备选择可以将其接至GPIO；BL为背光控制引脚，连接至3.3V可使其恒亮，若需要控制背光可以使用GPIO进行控制。


# LCD-1602-I2C
A simple Python library for displaying text on the LCD 1602 w/ I2C. Implemented on the **Raspberry Pi** 3 B.

## Simple Example
```python
from LCD import LCD

lcd = LCD() # params available for rPi revision, I2C Address, and backlight on/off
            # lcd = LCD(2, 0x3F, True)

lcd.message("Hello World!", 1) # display 'Hello World!' on line 1 of LCD

time.sleep(5) # wait 5 seconds

lcd.clear() # clear LCD display
```

## Install/Setup
```
sudo apt-get install i2c-tools
sudo apt-get install python-smbus
```

#### Enable I2C
`sudo raspi-config`
Advanced Options > I2C > Enable

#### Determine I2C Address
`i2cdetect -y 0`
default is 0x3F

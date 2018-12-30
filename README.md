# 4-channel Thermocouple PCB (MAX31855)
## Eagle CAD Schematic and PCB Layout
### Part Number PCB100 Rev A 

This design has 4 channels of **MAX31855** thermocouple amplifiers managed by 
an **STM32F042K4** (or **'K6**) ARM Cortex-M0 processor.  Primary communication
is RS-485 over Cat 5 UTP Ethernet cables with a POE-like power scheme (in the 
range of 5V to 12V). Both full and half-duplex communication schemes are 
supported.

Secondary communication is over an FTDI 232-TTL USB-to-UART cable.  Direct 
communiction over USB to the STM32 is also supported. Each allow an instance
of this board (perhaps without the MAX31855 populated) to be the RS-485 master
and provide POE-like power from a 2x5.5 mm power connector. 

A portion of this design was leveraged from the 
**_Adafruit Thermocouple Amplifier MAX31855 breakout board_**. 
See license copied below. Adafruit's support of open-source hardware is appreciated.

----------------------

Adafruit MAX31885 Thermocouple Amp breakout

These are the Eagle CAD files for the Adafruit MAX31885 Thermocouple Amp breakout:

  ----> http://www.adafruit.com/products/269

Adafruit invests time and resources providing this open source design, please support Adafruit and open-source hardware by purchasing products from Adafruit!

Thermocouples are very sensitive, requiring a good amplifier with a cold-compensation reference. The MAX31855K does everything for you, and can be easily interfaced with any microcontroller, even one without an analog input. This breakout board has the chip itself, a 3.3V regulator with 10uF bypass capacitors and level shifting circuitry, all assembled and tested. Comes with a 2 pin terminal block (for connecting to the thermocouple) and pin header (to plug into any breadboard or perfboard). Goes great with our 1m K-type thermocouple. 


All text above must be included in any redistribution

Designed by Limor Fried/Ladyada for Adafruit Industries.
Creative Commons Attribution/Share-Alike, all text above must be included in any redistribution


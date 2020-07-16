# 4-channel Thermocouple PCB (MAX31855)
## Eagle CAD Schematic and PCB Layout
### Part Number: PCB100 Rev A

This design has 4 channels of **MAX31855** thermocouple amplifiers managed by
an **STM32F042K4** (or **'K6**) ARM Cortex-M0 processor.  Primary communication
and power is RS-485 over Cat 5 UTP Ethernet cables with a POE-like power scheme.
Both full and half-duplex communication schemes are supported. 

Secondary communication is over an **FTDI 232-TTL USB-to-UART** cable.  Direct
communication over **USB** to the STM32 is also supported by the layout (but
has not been tested). Each allow an instance of this board (perhaps without the
MAX31855 populated) to be the RS-485 controller and provide POE power to the
bus from either the USB connection or a 2x5.5 mm power connector.

The RJ-45 Pinout is compatible with the 8-pin modular connector pinout in
**ANSI E1.11-2008 (R2018)** 
 _DMX512-A Asynchronous Serial Digital Data Transmission Standard_  
but has not been tested for interoperability. 

Please note the RS-485 signal naming in this design matches the IC 
manufacturers' convention (A is non-inverting, B is inverting) which is
opposite the RS-485/RS-422 standard (A is inverting, B is non-inverting).

The RJ-45 pins selected for power are also compatible with 10/100 Base-T
Power over Ethernet (POE) in case of a cabling error. External power in the
range of 5V to 12V is supported, but there is little thermal margin on the
LDO at 12V. Lower than 5V is possible if the voltage drop over the cable
is managed.


### Part Number: PCB101 Rev A 

This revision:

- Adds a TPS25921 eFuse to the 2x5.5 mm connector that sources the POE power
injection to ensure that it is current limited.
- Inverts the polarity of the user button so that it can be used for the SMT32
boot loader function.
- Moves the FTDI USART port to PA9/PA10 to support the SMT32 boot loader
function.
- Moves the I2C port to pins PB6/PB7 (USART and I2C were swapped).
- Adds 3 pairs of holes for each channel so that the thermocouple leads can be
tied to the PCB for strain relief.
- Lengthens the PCB.
- Corrects pinout error on button orientation.


## License: ##

[MIT License](../master/LICENSE.txt)

----------------------

A portion of this design was leveraged from the 
**Adafruit Thermocouple Amplifier MAX31855 breakout board**. 
The Adafruit license is copied below. I support Adafruit's open-source hardware.

> Adafruit MAX31885 Thermocouple Amp breakout
> 
> These are the Eagle CAD files for the Adafruit MAX31885 Thermocouple Amp
> breakout:
> 
>   ----> http://www.adafruit.com/products/269
> 
> Adafruit invests time and resources providing this open source design,
> please support Adafruit and open-source hardware by purchasing products
> from Adafruit!
> 
> Thermocouples are very sensitive, requiring a good amplifier with a
> cold-compensation reference. The MAX31855K does everything for you, and can
> be easily interfaced with any microcontroller, even one without an analog
> input. This breakout board has the chip itself, a 3.3V regulator with 10uF
> bypass capacitors and level shifting circuitry, all assembled and tested.
> Comes with a 2 pin terminal block (for connecting to the thermocouple) and pin header (to plug into any breadboard or > perfboard). Goes great with our 1m K-type thermocouple. 
> 
> 
> All text above must be included in any redistribution
> 
> Designed by Limor Fried/Ladyada for Adafruit Industries.
> Creative Commons Attribution/Share-Alike, all text above must be included in
> any redistribution
> 

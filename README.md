Pinouts for the v2 internet bridge. See unannotated images in the 'originals' directory.

Notes:
- I was not able to get the UART0 and UART1 to output anything at various baud rates.
- the pads can be easily traced to the STM32 pins using a multimeter in continuity mode. Lower 2nd pad from the left doesn't appear to be mapped to a pin on the STM32.
- Attaching SWCLK, SWIO, GND, RST, and VDD to an STM32 programmer (clone) works. STM32CubeProgrammer was able to read and dump the firmware without issues. No read protection seems to be set, at least on my board.
- Ghidra is able to parse the firmware binary. Select ARM Cortex little endian as the language when importing.

Disclaimer:
No guarantee, warranty, or liability is expressed or implied. The author and contributors assume no responsibility for any damages, losses, or issues arising from the use of this information.

License: CC0 1.0 Universal (CC-0). See LICENSE.md for the full license.

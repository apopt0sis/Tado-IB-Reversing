Pinouts for the v2 internet bridge. See unannotated images in the 'originals' directory.

Main chips: STM32F411CEU6, RF chip: TI CC110L. The large chip on the reverse side of the board is for ethernet, I believe.

Notes:
- I was not able to get the UART0 and UART1 to output anything at various baud rates.
- most of the pads can easily be traced to the STM32 pins using a multimeter in continuity mode.
- Attaching SWCLK, SWIO, GND, RST, and VDD to an STM32 programmer (clone) works. STM32CubeProgrammer was able to read and dump the firmware without issues. No read protection seems to be set, at least on my board.
- Ghidra is able to parse the firmware binary. Select ARM Cortex little endian as the language when importing.

Disclaimer:
No guarantee, warranty, or liability is expressed or implied. The author and contributors assume no responsibility for any damages, losses, or issues arising from the use of this information.

License: CC0 1.0 Universal (CC-0). See LICENSE.md for the full license.

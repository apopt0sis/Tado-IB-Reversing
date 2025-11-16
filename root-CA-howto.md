1. Dump the firmware using STM32CubeProgrammer. Dump the entire memory via Read all. 
2. Import the binary into Ghidra. Select "ARM Cortex 32" little endian (default) as the Language. Set image base as 0.
3. In the CodeBrowswer, navigate to address `00059ff0`. This is where the tado Root CA is stored in the firmware.

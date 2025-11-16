1. Dump the firmware using STM32CubeProgrammer. Dump the entire memory via Read all. 
2. Import the binary into Ghidra. Select "ARM Cortex 32" little endian (default) as the Language. Set image base as 0.
3. In the CodeBrowswer, navigate to address `00059ff0`. This is where the tado Root CA is stored in the firmware. It's a DER-encoded X.509 certificate, so the total size should be 639 bytes.
4. This means that the full certificate is from address `00059ff0` to address `0005a26e`. Select this range in the CodeBrowser and press O to output the file.
5. Select Raw Bytes as the file type, make sure "Selection Only" is selected and export the file. A window will pop up showing you the details of the saved file, make sure the size is 639 bytes.
6. Finally, you can confirm the dumped certificate with `openssl x509 -in /path/to/file.bin -inform DER -text -noout`

TODO: Figure out cert pinning bypass
There seems to be additional verification checks related to certificate pinning. 

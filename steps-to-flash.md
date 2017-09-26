1 - go to http://kbfirmware.com/ to build hex firmware file
2 - download AVRDUDESS and WinAVR - copy libusb files from WinAVR (4 of them) to the AVRDUDESS folder
3 - cd into the AVRDUDESS folder (using cygwin)
4 - prep the following command, changing the port number and filename of the hex
  ./avrdude -p atmega32u4 -P com5  -c avr109  -U flash:w:filename.hex
4 - as u plug in the board, short twice GND and RST quickly, should show up in Device Manager under Ports as '...Bootloader'. 
If it doesn't show with bootloader on the end, you have missed your window (8 seconds from shorting the circuit twice)
5 - Run the above command ASAP
6 - Should now work as a keyboard! Short 2 ports to test

TODO
- find libusb files
- see if plain AVRDUDE works
- do i need to unplug and replug?


Resources
https://deskthority.net/workshop-f7/how-to-use-a-pro-micro-as-a-cheap-controller-converter-like-soarer-s-t8448.html
https://www.reddit.com/r/MechanicalKeyboards/comments/64b7t6/help_flashing_hex_file_to_sparkfun_pro_micro/
http://i.imgur.com/wMNx2u6.png
https://github.com/nicinabox/lets-split-guide/blob/master/flashing.md
544455555544455555444

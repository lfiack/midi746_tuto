# midi746_tuto
Dirty USB Midi on STM32F746G-Disco based on mimuz-tuch

It just prints the notes and CC received from USB FS to the console. You can adapt it to whatever you want.
It can also send notes or CC to the computer, just search in the code.

Also, if you remove the call to processMidiMessage(), it won't be able to send or receive data, so don't do that.

The code is working , but it's quite dirty. Files will be modified if you gerate the code from the .ioc file. If you have to do so, just do the following:
1. Delete usbd_cdc_if.c and usbd_cdc_if.h
2. Copy and overwrite usb_device.c (in USB_DEVICE/App/)
3. Copy and overwrite usbd_core.c (in Middleware/ST/STM32_USB_Device_LIBRARY/Core/Src/)

All the USB MIDI part is copied from [Mimuz-tuch project](https://github.com/mimuz/mimuz-tuch). It's CC-BY so, hey, thanks!

Oh, and I did a [video](https://youtu.be/wbQv88xiTGY) (In French, of course): 

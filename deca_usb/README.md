# Tatung Einstein - DECA USB keyboard

This version is for testing the new ULPI USB module from @TheSonders https://github.com/TheSonders/USBKeyboard/blob/main/ULPI_PS2_PUBLIC.v

This is a standalone project that cannot be generated with the make script. It contains all Demistify components but is not in sync with the other Demistify board folders.

**Testing**

Please test all your USB keyboards and notify if it's working or not to @TheSonders via issue at his [repository](https://github.com/TheSonders/USBKeyboard/blob/main/ULPI_PS2_PUBLIC.v)

* If working please provide VID and PID codes of your keyboard (lsusb output codes in Linux)
* If not working try disconnecting power and/or program again the board (surely needs implementing the PLL locking)


The two switches SW0 and SW1 from Deca board are for toggling the NumLock and CapsLock leds.

**Requeriments**

* Deca board  
* USB keyboard (low speed). Low speed USB keyboards are the old ones and possibly the very cheap ones.
* A mini USB to USB A female adaptor is needed  to be connected into the USB connector next to HDMI.

* An SD card inserted is required (can be empty)
* HDMI video output

**Binaries**

* Binaries are found inside TatungEinstein_DeMiSTify/deca_usb/output_files folder

**Compile the project**

* Download zip project or `git clone https://github.com/DECAfpga/TatungEinstein_DeMiSTify`

* Open quartus and load project from TatungEinstein_DeMiSTify/deca_usb/TatungEinstein_deca.qpf

* Start compilation


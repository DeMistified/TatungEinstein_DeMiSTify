# Tatung Einstein - DECA USB keyboard

This version is for testing the new ULPI USB module from @TheSonders https://github.com/TheSonders/USBKeyboard/blob/main/ULPI_PS2_PUBLIC.v

This is a standalone project that cannot be generated with the make script. It contains all Demistify components but is not in sync with the other Demistify board folders.

**Testing**

Please test all your USB keyboards and notify how if it's working or not.  

* If working please provide VID and PID codes of your keyboard (lsusb output codes in Linux)
* If not working disconnect power and program again the board

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


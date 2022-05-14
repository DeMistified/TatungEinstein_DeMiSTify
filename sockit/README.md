# Tatung Einstein DeMiSTified - SoCkit port

13/05/22 SoCkit port DeMiSTified by Somhic from prior demistification for Deca by Somhic. Original MiSTer core https://github.com/MiSTer-devel/TatungEinstein_MiSTer/

[Read this guide if you want to know how I DeMiSTified this core](https://github.com/DECAfpga/DECA_board/tree/main/Tutorials/DeMiSTify).

**Features for Sockit board:**

* VGA video output (using only 666 but capable of 888)
* Audio I2S Line out (3.5 jack green connector) 

**Additional hardware**:

- PS/2 Keyboard connected to external addon  (see pinout below)
- Joystick available through external addon  (see pinout below).  

##### Versions:

v0.1 vga only

### STATUS

* Working fine




### Instructions to compile the project for a specific board:

(Note that sof/svf files are already included in /deca/output_files/)

```sh
git clone https://github.com/somhi/TatungEinstein_DeMiSTify/
cd TatungEinstein_DeMiSTify
#Do a first make (will finish in error) but it will download missing submodules 
make
cd DeMiSTify
#Create file site.mk in DeMiSTify folder 
cp site.template site.mk
#Edit site.mk and add your own PATHs to Quartus (Q18)
gedit site.mk
#Go back to root folder and do a make with board target (deca, neptuno, uareloaded, atlas_cyc). If not specified it will compile for all targets.
cd ..
make BOARD=sockit
#when asked just accept default settings with Enter key
```

After that you can:

* Flash bitstream directly from [command line](https://github.com/DECAfpga/DECA_binaries#flash-bitstream-to-fgpa-with-quartus)
* Load project in Quartus from /sockit/TatungEinstein_deca.qpf 

### Pinout connections:

Check the qsf  project file at the sockit folder.

I'm currently using the Terasic HSMC to GPIO [Daughter Board](https://www.digikey.es/es/products/detail/P0033/P0033-ND/2003485) connected to the [Deca Retro cape](https://github.com/somhi/DECA_retro_cape_2) to SoCkit gateway.   

* J3 2x40 pin is connected to Deca Retro cape to use its connector peripherals: ps2 keyboard, db9 joystick, pmod3 for a Pmod microSD

* J2 2x40 pin is for connecting [SDRAM Mister modules](http://modernhackers.com/128mb-sdram-board-on-de10-standard-de1-soc-and-arrow-sockit-fpga-sdram-riser/)  (not used in this core)

An specific addon for SoCkit might be developed in the future.

**Others:**

* Button KEY4 is a reset button

### OSD Controls

* F12 show/hide OSD 
* Long F12 toggles VGA/RGB mode
* The reset button KEY4 resets the controller (so re-initialises the SD card if it's been changed, reloads any autoboot ROM.) The OSD Reset menu item resets the core itself.


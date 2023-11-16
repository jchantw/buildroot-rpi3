# buildroot for Raspberry Pi 3

  Latest long term support release: 2023.02.7
  URL: https://buildroot.org/downloads/buildroot-2023.02.7.tar.gz

  Step 1. make list-defconfigs

  Step 2. make raspberrypi3_defconfig

  Step 3. make menuconfig

Toolchain ---> Toolchain type ---> Enter ---> External toolchain ---> <Select>
          ---> Toolchain (Arm ARM 2021.07) ---> Enter ---> Custom toolchain ---> <Select>
		  ---> Toolchain origin (Pre-installed toolchain)
		  ---> Toolchain path ---> Enter ---> Type /usr/local/arm/ ---> < Ok >
		  ---> ($(ARCH)-linux) Toolchain prefix ---> Enter ---> Type $(ARCH)-linux-gnueabihf ---> < Ok >
          ---> External toolchain gcc version (12.x) ---> Enter ---> 9.x ---> <Select>
		  ---> External toolchain kernel headers series (2.6.x) ---> Enter ---> 4.9.x ---> <Select>
		  ---> External toolchain C library (uClibc/uClibx-ng) ---> Enter ---> glibc ---> <Select>
		  ...
		  Space to [*] Toolchain has C++ support?
		  ...
		  Space to [*] Copy gdb server to the Target
		  
		  < Exit >

Build options ---> gcc optimization level (optimize for size) ---> optimize for debugging ---> <Select>

		  < Exit >   

Kernel ---> $(call github,raspberrypi,linux,0b54dbda3cca2beb51e236a25738784e90853b64)/linux-0b54dbda3cca2beb51e236a25738784e90853b64.tar.gz
       ---> $(call github,raspberrypi,linux,7f9c648dad6473469b4133898fa6bb8d818ecff9)/linux-7f9c648dad6473469b4133898fa6bb8d818ecff9.tar.gz
       
	   Kernel 4.9.80
	   
	   https://github.com/raspberrypi/linux/commits/rpi-4.9.y-stable
	   [Verified] commit ID 921b6254452db87ae0304beaa9833cfdf5083ed8 is refer to /raspberrypi/linux/commits/rpi-4.9.y-stable
	   
	   https://github.com/raspberrypi/linux/commits/rpi-4.9.y
	   commit ID 7f9c648dad6473469b4133898fa6bb8d818ecff9 is refer to /raspberrypi/linux/commits/rpi-4.9.y
	   
		  < Exit >  


  Step 4.



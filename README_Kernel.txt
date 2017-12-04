################################################################################

1. How to Build
	- get Toolchain
		From android git server , codesourcery and etc ..
		 - android/prebuilts/gcc/linux-x86/arm/arm-eabi-4.8/bin/arm-eabi-
	

	- edit Makefile
		edit "CROSS_COMPILE" to right toolchain path(You downloaded).
		  EX)  tool:cross-compile = android/prebuilts/gcc/linux-x86/arm/arm-eabi-4.8/bin/arm-eabi- 
          Ex)  CROSS_COMPILE=/usr/local/toolchain/aarch64-linux-android-4.9/bin/aarch64-linux-android-          // check the location of toolchain
  			
		$ make  gtexswifi-dt_defconfig
		$ make -j64

2. Output files
	- Kernel : out/arch/arm64/boot/Image
	- module : out/drivers/*/*.ko

3. How to Clean	
		Change to OUTPUT_DIR folder
		EX) $(pwd)/out
		$ make clean
################################################################################

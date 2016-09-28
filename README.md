# openwrt-dir605a2
OpenWrt for D-Link DIR-605 A2

### Warning

This OpenWrt patch for D-Link DIR-605 A2 is NOT thoroughly tested. It could damage your router at worst circumstances.

### Usage

1. Prepare a Linux 64-bit system, as demanded by OpenWrt Image Builder.

2. Download OpenWrt image builder

    [chaos_calmer 15.05.1](https://downloads.openwrt.org/chaos_calmer/15.05.1/ramips/rt288x/OpenWrt-ImageBuilder-15.05.1-ramips-rt288x.Linux-x86_64.tar.bz2)

3. Extract OpenWrt-ImageBuilder-15.05.1-ramips-rt288x.Linux-x86_64.tar.bz2

    Copy dir605a2.patch file to the same directory as the OpenWrt-ImageBuilder-15.05.1-ramips-rt288x.Linux-x86_64 folder.

4. Execute

	> ls
	
	There should be two items at current directory:
	
	*OpenWrt-ImageBuilder-15.05.1-ramips-rt288x.Linux-x86_64*
	
	*dir605a2.patch*
	
    > patch -p0 < dir605a2.patch
    
    > cd OpenWrt-ImageBuilder-15.05.1-ramips-rt288x.Linux-x86_64
    
    > make image PACKAGES="luci" FILES="./target/linux/ramips/base-files"

5. Flash your router whih the generated bin file.

    *OpenWrt-ImageBuilder-15.05.1-ramips-rt288x.Linux-x86_64/bin/ramips/openwrt-15.05.1-ramips-rt288x-dir-605-a2-squashfs-factory.bin*

6. A manual restart of the router may be required. Then navigate to 192.168.1.1.

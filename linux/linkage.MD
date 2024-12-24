C | A
-|-
nm | Print symbols
ldd | Check dependencies
ldd \| grep not | Check missing dependencies
cat /etc/ld.so.conf | Conf file for folders for the linker to look in
/etc/ld.so.conf.d | Folders for the linker to look in

### Add persistent relative path for the linker (persistent LD_LIBRARY_PATH)
C | A
-|-
readelf -d my.so | Read RPATH / RUNPATH
patchelf --set-rpath '$ORIGIN' my.so | Edit the rpath and add the $ORIGIN - folder that contains the so 
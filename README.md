fpin sample
==

mkdir bin-arm-none-eabi build-aux m4
autoreconf -vi
cd bin-arm-none-eabi
CFLAGS='' LDFLAGS='--specs=rdimon.specs' ../configure
make all

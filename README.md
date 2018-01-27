fpin sample (based on the fpin sample of arm-none-eabi)
==

The original fpin sample is usually located at `/usr/share/doc/gcc-arm-none-eabi/examples/src/fpin`

# The build commands

    mkdir bin-arm-none-eabi build-aux m4
    autoreconf -vi
    cd bin-arm-none-eabi
    CFLAGS='' LDFLAGS='--specs=rdimon.specs' ../configure
    make all

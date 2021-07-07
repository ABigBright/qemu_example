# Command

```sh
/home/briq/studio/zephyr-sdk-0.11.4/sysroots/x86_64-pokysdk-linux/usr/bin/qemu-system-arm \
    -cpu cortex-m3 \
    -machine lm3s6965evb \
    -nographic \
    -vga none \
    -net none \
    -pidfile qemu.pid \
    -chardev stdio,id=con,mux=on \
    -serial chardev:con \
    -mon chardev=con,mode=readline \
    -icount shift=6,align=off,sleep=off \
    -rtc clock=vm \
    -kernel /home/briq/studio/zephyrproject/zephyr/build/zephyr/zephyr.elf

```

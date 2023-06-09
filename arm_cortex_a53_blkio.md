```sh
qemu-system-aarch64 -cpu cortex-a53 \
    -m 512 \
    -smp 4 \
    -machine virt \
    -kernel a.elf \
    -net none \
    -nographic \
    -drive if=none,file=./a.out,id=blk,format=raw \
    -device virtio-blk-device,drive=blk
```

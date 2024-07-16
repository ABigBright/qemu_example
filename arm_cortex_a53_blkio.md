# 方式一

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

# 方式二

```sh
qemu-system-aarch64 -cpu cortex-a53 \
        -m 512 \
        -smp 4 \
        -machine virt \
        -kernel out/oneos.elf \
        -net none \
        -nographic \
        -blockdev driver=file,node-name=blk_1_file,filename=./linker.lds \
        -blockdev driver=raw,node-name=blk_1,file=blk_1_file \
        -device virtio-blk-device,drive=blk_1
```

上面两种不同的命令写法, 本质是一样的, 实现同样的效果

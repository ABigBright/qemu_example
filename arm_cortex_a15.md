# Command

```sh
qemu-system-arm \
    -cpu cortex-a15 \
    -m 512 -smp 1 \
    -machine virt,highmem=off \
    -kernel build-qemu-virt-arm32-test/lk.elf \
    -net none -nographic
```
> 有关-M 选项，可以参考qemu/virt.rst中的使用说明

# Command

```sh
qemu-system-aarch64 \
    -M virt,secure=on,gic-version=3 \
    -m 512M \
    -nographic \
    -kernel ~/studio/zephyr_proj/zephyr/build/zephyr/zephyr.elf \
    -cpu cortex-a53 -s -S

```
> 有关-M 选项，可以参考qemu/virt.rst中的使用说明

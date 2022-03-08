# Command

```sh
qemu-system-x86_64 \
    -M q35 \
    -m 1G \
    -cpu host \
    -accel kvm \
    -cdrom ~/work/soft_setup/setup_package/os/Win10_20H2_v2_Chinese\(Simplified\)_x64.iso \
    -monitor stdio \
    -vga none \
    -device ramfb \
    -blockdev driver=file,node-name=disk_qcow2,filename=./disk.qcow2 \
    -blockdev driver=qcow2,node-name=disk1_qcow2,file=disk_qcow2 \
    -device nvme,drive=disk1_qcow2,serial="dummyserial",bootindex=1 \
    -blockdev driver=file,node-name=virtio_iso,filename=/home/briq/work/soft_setup/setup_package/kvm/virtio-win-0.1.190.iso \
    -device ide-cd,drive=virtio_iso
```

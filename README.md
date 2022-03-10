### How-To-Compile-and-Flash
```

$cd tinyusb/examples/device/hid_composite_freertos
$idf.py -B_build/esp32s2_saola_1 -DFAMILY=esp32s2 -DBOARD=espressif_saola_1 -p /dev/ttyUSB0 flash monitor
```
or
```
esptool.py esp32s2 -p /dev/ttyUSB0 -b 460800 --before=default_reset --after=hard_reset write_flash --flash_mode dio --flash_freq 80m --flash_size 2MB 0x8000 partition_table/partition-table.bin 0x1000 bootloader/bootloader.bin 0x10000 espressif_saola_1-hid_composite_freertos.bin

```

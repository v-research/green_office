# Micropython Installation Guide

## 0. disconnect everything from espXX except the USB cable (of course :D)

## 1. if pip is not installed on pc

pip install esptool

## 2. erase espXX memory

esptool.py --port COMxx erase_flash
esptool.py --port COM10 erase_flash

## 3. flash micropython firmware

esptool.py --port COMxx --baud 460800 write_flash --flash_size=detect 0x1000 esp32_file_name.bin
esptool.py --port COM10 --baud 460800 write_flash --flash_size=detect 0x1000 esp32-20210623-v1.16.bin

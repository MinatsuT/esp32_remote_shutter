# ESP32 Bluetooth Remote Shutter for a Smartphone Camera
## Pre-requirements
Before compile this project, please install [ESP-IDF](https://github.com/espressif/esp-idf) and set `$(IDF_PATH)`:

`% export IDF_PATH=/your/esp-idf/path`

## How to compile
1. Clone the [BTstack](https://github.com/bluekitchen/btstack).
```
% cd ~/esp
% git clone https://github.com/bluekitchen/btstack.git
```
2. Clone this project into "btstack/port/esp32", and copy "components" and "sdconfig" from the templete directory.
```
% cd btstack/port/esp32
% git clone https://github.com/MinatsuT/esp32_remote_shutter.git
% cp -r template/components esp32_remote_shutter
% cp template/sdkconfig esp32_remote_shutter
```
3. Edit serial configurations according to your environment.
```
% cd esp32_remote_shutter
% make menuconfig
```
4. Compile, flash and start monitoring.
```
% make flash monitor
```

## How to use.
- Scan BT devices from your smartphone and establish a connection to the "ESP32 Remote Shutter" device.
- Start camera app on your smartphone.
- Push "enter" from the above monitor, then shutter code (Volume Up) will be sent.


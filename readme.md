# "Stock Clock" Klipper Configuration Files

## About

This repository contains a ready-to-go Klipper configuration for a modified Ender 5:

- Dependencies: MainsailOS
- MCU: BIGTREETECH Octopus 1.1
- Drivers: TMC2209
- Hotend: (Mk8 Compatible)
- Extruder: (Creality stock equivalent)
- Build Volume: Stock 220x220x300mm
- Display: Stock Creality 12864
- Steppers: Stock Creality
- Fans:
  - Hotend fan (24V)
  - Part cooling fan (24V)
  - Electronics: 2 fans (12V)
  - Chamber: 2 fans (disabled by default)
- Thermistors:
  - Hotend
  - Bed
  - Chamber (disabled by default)
  - Electronics Case
- ABL: BLTouch (disabled by default)
  
## Example Usage

From a shell on your Raspberry Pi:

```
cd ~/klipper_config
git clone https://github.com/jon-harper/stock-clock config
```

Modify your `printer.cfg` so that it looks like this:

```
[include mainsail.cfg]

[mcu]
serial: #ex: /dev/serial/by-id/usb-Klipper_stm32[...]
restart_method: command

[include config/main.cfg]

# Any final configuration declarations or inclusions
```
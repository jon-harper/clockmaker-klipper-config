# Clock 3 Klipper Configuration Files

## About

This repository contains a ready-to-go Klipper configuration for a modified Ender 5:

- Dependencies: MainsailOS
- MCU: BIGTREETECH SKR 2.0 Rev B
- Drivers: TMC2209
- Hotend: MicroSwiss All-Metal Hotend or clone
- Build Volume: 220x220x300mm
- Display: Stock Creality 12864
- Steppers: Stock Creality
- Lights: 28 WS2815 LEDs, using the Neopixel pin
- Fans:
  - Hotend fan (24V)
  - Part cooling fan (24V)
  - Chamber: 2 blowers (24V)
  - Electronics: 1 fan (12V)
  
This is the Thingiverse page with the modifications for this printer: [Mirrored Ender 5](https://www.thingiverse.com/thing:5146291).

## Example Usage

From a shell on your Raspberry Pi:

```
cd ~/klipper_config
git clone https://github.com/jon-harper/clockmaker-klipper config
```

Modify your `printer.cfg` so that it looks like this:

```
[include mainsail.cfg]

[mcu]
serial: #ex: /dev/serial/by-id/usb-Klipper_stm32f407xx_190031000C47393437313133-if00
restart_method: command

[include config/main.cfg]

# Any final configuration declarations or inclusions
```
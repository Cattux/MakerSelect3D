# Maker Select 3D

This repo contains the modifications and current configuration files for my Monoprice Maker Select 3D v2 which is a rebranded Wanhao Duplicator i3 v2.1.

## Main Board

The main board in this printer is an BTT SKR-Mini E3 V2.0.

## Screen

The screen is still the stock screen. A custom cable was created so that it could work with the new main board, see pinout below:

| LCD Pin | SKR Pin | Description    |
| ---     | :--     | :--            | 
| 1       | 7       | CS             | 
| 2       | 3       | Encoder B      | 
| 3       | 8       | LCD Data       | 
| 4       | 5       | Encoder A      | 
| 5       | 6       | SCLK           | 
| 6       | 2       | Encoder Button | 
| 7       | 4       | estop (RST)    | 
| 8       | 1       | Beeper         | 
| 9       | 10      | 5V             | 
| 10      | 9       | GND            | 

## Bed Heater

The stock bed heater is being used, but is powered through an external MOSFET. This was required when using the Melzi board, not 100% sure if it's required for the SKR but it's not hurting anything being there.

## Build Plateform

A 220x220mm piece of glass is used for the build plate.

## BLTouch

A BLTouch is being used instead of the stock Z end stop. It is mounted with this STL:

https://www.thingiverse.com/thing:1762801

## Part Cooler

 The stock cooler was replaced with the DIICooler and a 50mm radial fan, STL link below:
 
https://www.thingiverse.com/thing:1025471

## Hotend Cooler

Currently I have the stock 40mm fan for the hotend cooling, but it is grossly inadequate so there is also a 50mm radial fan temporarially mounted with super gluie until a better mounting system has been designed and/or printed.



## Firmware

Klipper is loaded onto this printer, see [printer.cfg](printer.cfg)

It is running on a Raspberry Pi 3B which has been mounted inside of the control box and is powered from the SKR with a DCDC converter to drop the voltage to 5V.

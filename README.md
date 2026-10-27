# Royalpad
A Custom 9-key Macropad with an EC11 Rotary Encoder, 0.91-inch OLED Display, and Custom KiCad PCB Built for Productivity.

## Overview
Royalpad is a custom macropad that uses the Seeed Studio XIAO RP2040, QMK firmware, and brings nine mechanical MX switches, a clickable rotary encoder, and a small OLED display. Whether you're coding, CADding, trying to be productive, or doomscrolling optimally, this macropad is the tool for the job.

## Renders
<img width="907" height="847" alt="image" src="https://github.com/user-attachments/assets/25aa61c1-e91a-4615-b7ee-3300288bf8f2" />

<img width="958" height="766" alt="Screenshot 2026-10-18 150451" src="https://github.com/user-attachments/assets/abbcaa90-8268-4482-a9d3-2912049517df" />

<img width="790" height="738" alt="image" src="https://github.com/user-attachments/assets/8f14fbac-f575-4f26-b72c-479bee5ed762" />

<img width="1058" height="843" alt="image" src="https://github.com/user-attachments/assets/0fc735e7-6182-4310-a8e7-f0eeb79ef4f4" />

<img width="1332" height="631" alt="image" src="https://github.com/user-attachments/assets/eb984ab8-1d3b-4384-a45c-830667accc95" />

<img width="627" height="792" alt="image" src="https://github.com/user-attachments/assets/f4535649-75a5-4a4e-9607-8a0dc5bca35f" />


## Features
- 3x3 Matrix Layout: A compact 3 × 3 grid of mechanical switches.
- EC11 Rotary Encoder: Provides rotational input and a push-button click.
- 0.91-inch OLED Display: A small screen for status or other information.
- XIAO RP2040 Controller: A compact microcontroller board for the macropad.
- Custom PCB: Designed in KiCad.
- QMK Firmware: open-source firmware for maximum control

## Bill of Materials (BOM)

| Component | Quantity | Specifications | Source / Notes |
|---|---:|---|---|
| Seeed XIAO RP2040 | 1 | Unsoldered microcontroller board | [Seeed Studio Documentation](https://wiki.seeedstudio.com/XIAO-RP2040/) |
| 1N4148 Diodes | 9 | Through-hole diodes, one per switch | [Vishay Datasheet](https://www.vishay.com/docs/81857/1n4148.pdf) |
| MX-Style Switches | 9 | Mechanical keyboard switches | [Switch Datasheet](https://cdn.shopify.com/s/files/1/0565/8070/2297/files/SPEC-KS-3Y10B050NW-X1-Yellow_Switch.pdf?v=1675841028) |
| EC11E Rotary Encoder | 1 | Incremental rotary encoder with integrated push button | [Encoder Datasheet](https://mm.digikey.com/Volume0/opasdata/d220001/medias/docus/6727/alps_alps-s-a0008379064-1-1733314-1-13.pdf) |
| 0.91-inch OLED Display | 1 | Compact display module | Provided by Hack Club |
| White Blank DSA Keycaps | 9 | Blank DSA-profile keycaps compatible with the selected switches | White, unlabelled keycaps - Provided by Hack Club |
| M3 × 16 mm Screws | 4 | Enclosure mounting fasteners | Provided by Hack Club |
| Custom PCB | 1 | Custom-designed Royalpad circuit board | Designed in KiCad |
| 3D-Printed Top Case | 1 | Upper enclosure for the macropad | Designed in SolidWorks |
| 3D-Printed Bottom Case | 1 | Lower enclosure housing the PCB and electronics | Designed in SolidWorks |
| Rotary Encoder Knob | 1 | Knob compatible with the EC11E encoder shaft | Provided by Hack Club |

# Royalpad
A Custom 9-key Macropad with an EC11 Rotary Encoder, 0.91-inch OLED Display, and Custom KiCad PCB Built for Productivity. Royalpad was made as a submission for [Hackpad V5](https://hackpad.hackclub.com/) through the Stardance challenge.

## Overview
Royalpad is a custom macropad that uses the Seeed Studio XIAO RP2040, QMK firmware, and brings nine mechanical MX switches, a clickable rotary encoder, and a small OLED display. Whether you're coding, CADding, trying to be productive, or doomscrolling optimally, this macropad is the tool for the job.

## Renders
<img width="907" height="847" alt="image" src="https://github.com/user-attachments/assets/25aa61c1-e91a-4615-b7ee-3300288bf8f2" />

<img width="958" height="766" alt="Screenshot 2026-10-18 150451" src="https://github.com/user-attachments/assets/abbcaa90-8268-4482-a9d3-2912049517df" />

<img width="790" height="738" alt="image" src="https://github.com/user-attachments/assets/8f14fbac-f575-4f26-b72c-479bee5ed762" />

<img width="1058" height="843" alt="image" src="https://github.com/user-attachments/assets/0fc735e7-6182-4310-a8e7-f0eeb79ef4f4" />

<img width="1322" height="588" alt="Screenshot 2026-10-28 180010" src="https://github.com/user-attachments/assets/03c23a93-e986-4646-99ac-b22c0ffd6d2f" />

<img width="627" height="792" alt="image" src="https://github.com/user-attachments/assets/f4535649-75a5-4a4e-9607-8a0dc5bca35f" />


## Features
- 3x3 Matrix Layout: A compact 3 × 3 grid of mechanical switches.
- EC11 Rotary Encoder: Provides rotational input and a push-button click.
- 0.91-inch OLED Display: A small screen for status or other information.
- XIAO RP2040 Controller: A compact microcontroller board for the macropad.
- Custom PCB: Designed in KiCad.
- QMK Firmware: open-source firmware for maximum control
- A cool case with triangle cutouts, because why not?

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


## Firmware overview
RoyalPad uses QMK firmware to turn its nine-key macropad into five different shortcut layers. The active layer determines what each key and the rotary encoder do. The OLED displays the active mode and provides an on-screen menu for switching between modes.
Main firmware features
- Five modes: Main, Productivity, SOLIDWORKS, Coding and KiCad.
- OLED display: Shows the active mode and the mode-selection menu.
- Rotary encoder mode selector: Hold the encoder's push switch for five seconds to open the menu, rotate to move through the options, then press the encoder to select a mode.
- Mode-specific encoder controls: The encoder changes behaviour depending on the selected mode.
- Custom shortcuts: Key functions target common actions in everyday computer use, productivity applications, CAD, coding and PCB design.
Mode-specific key functions
The table below uses a left-to-right, top-to-bottom key order, from K1 to K9.

### Layer 0: Main

| Key | Function |
|---|---|
| K1 | Copy |
| K2 | Paste |
| K3 | Undo |
| K4 | Cut |
| K5 | Save |
| K6 | Select All |
| K7 | Previous Track |
| K8 | Play/Pause |
| K9 | Next Track |

**Rotary Encoder:** Turn to control system volume. Short press to mute or unmute.

### Layer 1: Productivity

| Key | Function |
|---|---|
| K1 | Open Notion |
| K2 | Open ChatGPT |
| K3 | Open Gmail |
| K4 | Screenshot |
| K5 | Open Study Focus Pomodoro |
| K6 | Clipboard |
| K7 | Calendar |
| K8 | New Tab |
| K9 | Task View |

**Rotary Encoder:** Page Up / Page Down navigation.

### Layer 2: SOLIDWORKS
**Note:** The first eight commands use custom `Ctrl + Alt + 1` through `Ctrl + Alt + 8` shortcuts configured in SOLIDWORKS. Zoom to Fit uses the standard `F` shortcut.

| Key | Function |
|---|---|
| K1 | Start Sketch |
| K2 | Smart Dimension |
| K3 | Line |
| K4 | Corner Rectangle |
| K5 | Sketch Fillet |
| K6 | Trim Entities |
| K7 | Linear Sketch Pattern |
| K8 | Exit Sketch |
| K9 | Zoom to Fit |

**Rotary Encoder:** Mouse-wheel viewport zoom.


### Layer 3: Coding

| Key | Function |
|---|---|
| K1 | Open GitHub |
| K2 | Open Visual Studio Code |
| K3 | Open Terminal |
| K4 | Copy |
| K5 | Paste |
| K6 | Cut |
| K7 | Undo |
| K8 | Redo |
| K9 | Save |

**Rotary Encoder:** Page Up / Page Down navigation.

### Layer 4: KiCad

| Key | Function |
|---|---|
| K1 | Add Footprint |
| K2 | Route Tracks |
| K3 | Properties |
| K4 | Move |
| K5 | Rotate |
| K6 | Flip Footprint |
| K7 | Save |
| K8 | Refill Zones |
| K9 | Open 3D Viewer |

**Rotary Encoder:** Switch between the `B.Cu` and `F.Cu` copper layers.

## Additional Notes
- Some SOLIDWORKS shortcuts require separate configuration within SOLIDWORKS.
- Application-launch keys depend on the configured URLs or applications.
- KiCad shortcuts may vary depending on the active editor and shortcut configuration.
- Firmware updates require compiling and flashing a new .uf2 file.

A huge thank you to **Stardance and Hack Club** for providing such an awesome opportunity to design, build, and share a custom hardware project through the Hackpad Challenge!

Royalpad was my first time designing a custom PCB and building a custom hardware project. Throughout the process, I learned how to design and lay out a PCB using KiCad, including working with components such as MX-style switches, diodes, and a rotary encoder. I also used SOLIDWORKS to design a custom two-piece enclosure that fits the PCB and other components nicely. Beyond the hardware itself, this project gave me the opportunity to explore firmware and learn more about how software interacts with custom electronics. It was a great introduction to QMK firmware, as it was definitely a challenge to compile and code everything my Royalpad needed, especially for the various mode layers. I took inspiration from ReuTheCoder's [Stratum](https://github.com/ReuTheCoder/stratum-macropad) in terms of how it utilizes different layers where each key performs a different function.

Most importantly, Royalpad gave me the confidence to take on a project that was completely new to me, work through unfamiliar tools and challenges, and develop skills that I can carry into future electronics, CAD, and engineering projects. I'm really grateful to Hack Club and Stardance for making this experience possible!

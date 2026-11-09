# PCB_Designs
PCB designs in KiCad: schematics, layouts and manufacturing files

# PCB Designs

Welcome! This repository collects the **printed circuit boards I design in KiCad**, from simple learning circuits to complete boards ready for manufacturing.

I'm an Electronics and Communication Engineering student, and I use these projects to learn hardware design end to end: choosing components, drawing schematics, laying out boards, and preparing the files a manufacturer needs. Each design is documented so it's clear what it does, how it works, and why it's built the way it is.

---

## 🧭 What you'll find here

Every project lives in its own folder and includes:

- **Schematic:** the circuit, organised into labelled functional blocks
- **PCB layout:** the physical board design
- **Gerber and drill files:** everything needed to have the board manufactured
- **Images:** schematic, layout and 3D renders
- **README:** a detailed explanation of the design, components, calculations and assembly

```text
project-name/
├── project-name.kicad_pro   KiCad project
├── project-name.kicad_sch   Schematic
├── project-name.kicad_pcb   PCB layout
├── gerbers/                 Manufacturing files
├── images/                  Schematic, layout and 3D render
└── README.md                Full project documentation
```

---

## 🛠️ Design approach

- **Functional blocks:** schematics are split into clearly labelled sections (power, timing, output…) so they're easy to follow
- **Design rule checks:** each board is checked with KiCad's ERC (schematic) and DRC (layout) before export
- **Good layout habits:** ground pours, decoupling capacitors placed next to ICs, and wider traces for power
- **Documented calculations:** component values are explained, not just listed

**Tools:** KiCad 10 (schematic capture, PCB layout, 3D view, Gerber export)

---

## 📂 Projects

### 1. 555 Timer LED Blinker

📁 [`555-timer-led-blinker`](./555-timer-led-blinker) · **Status:** Ready for fabrication

![555 Timer LED Blinker](555-timer-led-blinker/images/3d-render.png)

A compact 9 V board that flashes an LED about **once per second** using the classic **NE555 timer** in astable mode. No microcontroller or code is involved: two resistors and a capacitor set the timing, and the chip switches the LED on and off by itself.

| | |
|---|---|
| **Core IC** | NE555P timer (DIP-8) |
| **Function** | Astable oscillator driving an LED |
| **Blink rate** | ≈ 1.05 Hz, ≈ 50% duty cycle (calculated) |
| **Supply** | 9 V battery |
| **Board** | 18.6 × 26.3 mm, 2 layers, all through-hole |

**Key design points**
- Timing set by R1 = 1 kΩ, R2 = 68 kΩ and C1 = 10 µF for an almost even on/off blink
- 100 nF decoupling capacitor beside the 555 to absorb its switching current spikes
- 10 nF capacitor on the control pin to keep the timing stable
- Ground pour on the bottom layer and wider power traces

**What I learned:** how the 555's comparators, flip-flop and discharge transistor create oscillation, how to calculate timing components, and the complete KiCad flow from schematic to Gerber files.

➡️ **[Read the full project documentation](./555-timer-led-blinker)**

---



## 🔗 More of my work

- 🌐 **Portfolio:** (add your website link here)
- 💼 **LinkedIn:** [Shalmali Mankikar](https://www.linkedin.com/in/shalmali-mankikar-51812325a/)

---

## © Copyright

© 2026 Shalmali Mankikar. All rights reserved.
These files are shared publicly for viewing and reference only. No permission is granted to copy, modify, manufacture, sell or redistribute them, in whole or in part, without my written permission.

These files are shared publicly for **viewing and reference only**. No permission is granted to copy, modify, manufacture, sell or redistribute them, in whole or in part, without my written permission.

# DDS Frequency Generator

> KiCad PCB Design | 2-Layer Board | AD9833 + ATmega328A

---

## Project Description
A Direct Digital Synthesis (DDS) frequency generator PCB designed using **KiCad**. The board uses the **AD9833BRMZ** DDS IC controlled by an **ATmega328A** microcontroller over SPI to generate sine, triangle, and square waveforms. A **24MHz CFPS-72 reference oscillator** provides precise clocking, and an **LM318M high-speed op-amp** conditions the output signal for a coaxial connector.

**Short Description (≤350 chars):**
> DDS-based frequency generator PCB using AD9833 + ATmega328A. Generates sine/triangle/square waves controlled via SPI. Includes LM318M output amplifier, 24MHz reference oscillator, and coaxial output. Designed in KiCad.

---

## Key Components

| Component | Description |
|-----------|-------------|
| **AD9833BRMZ-REEL** | DDS waveform generator – sine/triangle/square via SPI |
| **ATmega328-A** | MCU controller for AD9833 frequency register writes |
| **CFPS-72 24MHz** | Precision crystal oscillator – DDS reference clock |
| **LM318M** | High-speed op-amp for output signal amplification |
| **AMS1117-5.0** | 5V LDO regulator |
| **Potentiometers (2x)** | Frequency and amplitude adjustment |
| **SW_SPDT** | Waveform selection switch |
| **Coaxial Connector** | RF signal output |

---

## Design Features
- AD9833 generates sine, triangle, and square waveforms digitally
- ATmega328A programs AD9833 frequency/phase registers over SPI
- CFPS-72 24MHz reference oscillator provides stable DDS clock
- LM318M op-amp output stage for signal conditioning and drive
- Dual ±12V supply for op-amp headroom
- Potentiometers allow analog frequency fine-tuning

---

## Signal Flow
```
ATmega328A – MCU Controller
       ↓ SPI (MOSI/CLK/CS)
  AD9833 – DDS Waveform Generator
       ↓
  LM318M – Output Amplifier
       ↓
  Waveform Select Switch (SW_SPDT)
       ↓
  Coaxial Output Connector
       ↑
  AMS1117-5.0 ← 5V Supply
  ±12V Supply ← Dual Rail Power Input
```

---

## Files Included
- Frequency_Generator_A.kicad_sch – Schematic
- Frequency_Generator_A.kicad_pcb – PCB Layout
- Frequency_Generator_A-backups/ – Auto-backup files

---


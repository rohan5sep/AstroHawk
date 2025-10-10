# Raspberry Pi based inbuilt guider-computer (AstroHawk)

- [Raspberry Pi based inbuilt guider-computer (AstroHawk)](#raspberry-pi-based-inbuilt-guider-computer-astrohawk)
  - [Introduction](#introduction)
  - [Motivation](#motivation)
  - [Goals](#goals)
    - [Simplify cabling](#simplify-cabling)
    - [Compact & cost-effective design](#compact--cost-effective-design)
    - [Future expandability](#future-expandability)
    - [Dual use: astrophotography & visual observing](#dual-use-astrophotography--visual-observing)
  - [Vision](#vision)
  - [Technical Architecture (Conceptual Block Diagram)](#technical-architecture-conceptual-block-diagram)
  - [INDIGO Sky with ccd RPi](#indigo-sky-with-ccd-rpi)

## Introduction

This project is my attempt to design and build a compact, low-cost astrophotography station that combines a guider and a mount computer into a single unit.

## Motivation

One of the biggest challenges in astrophotography is the cable mess—USB hubs, dangling power cables, and multiple computers add unnecessary complexity. Commercial guiders and PC-based solutions solve some of these problems, but they are often expensive and not very customizable.

## Goals

### Simplify cabling

- Instead of connecting the guide camera over USB, the system uses the CSI (Camera Serial Interface) port of the Raspberry Pi, reducing reliance on extra hubs and potentially minimizing issues caused by snagging cable.

### Compact & cost-effective design

- The guider and the control computer are integrated into a single form factor.
- The system is designed to be budget-friendly, using widely available components while delivering performance at par with commercial astro-computers.

### Future expandability

- Planned support for 12V DC power ports to power accessories directly from the guider unit.
- Modular design to add or swap sensors and cameras as needed.

### Dual use: astrophotography & visual observing

- Provides GoTo mount control for telescope pointing.
- Can act as a “single box” solution whether you’re observing visually or imaging.

## Vision

The end result is a self-contained guiding and control hub that mounts directly on the telescope, minimizes external cabling, and makes setup in the field faster and more reliable. It should offer the usability of commercial astro-stations but with the flexibility and affordability of a DIY build.

## Technical Architecture (Conceptual Block Diagram)

          ┌──────────────────────────────────────┐
          │           Power Input (12V DC)       │
          └───────────────┬──────────────────────┘
                          │
                ┌─────────┴─────────┐
                │   Power Module    │
                │  (Regulation +    │
                │   12V DC outputs) │
                └─────────┬─────────┘
                          │
            ┌─────────────┴────────────────┐
            │     Raspberry Pi (Core)      │
            │                              │
            │ • CSI port → Guide Camera    │
            │ • USB/Ethernet → Mount Ctrl  │
            │ • WiFi/SSH → Remote Control  │
            │ • GPIO → Future sensors      │
            └─────────────┬────────────────┘
                          │
              ┌───────────┴───────────┐
              │    Telescope Mount    │
              │  (GoTo + Guiding I/F) │
              └───────────────────────┘

## INDIGO Sky with ccd RPi

RaspberryPI image with a pre-configured INDIGO server. This version of OS comes bundled with CCD RPi driver along with the stock drivers that come with the original INDIGO Sky OS.

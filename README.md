# AstroHawk

DIY Astro-Station with Inbuilt Guider

This project is my attempt to design and build a compact, low-cost astrophotography station that combines a guider and a mount computer into a single unit.

## Motivation

One of the biggest challenges in astrophotography is the cable mess—USB hubs, dangling power cables, and multiple computers add unnecessary complexity. Commercial guiders and PC-based solutions solve some of these problems, but they are often expensive and not very customizable.

## Goals

1. Simplify cabling

    1. Instead of connecting the guide camera over USB, the system uses the CSI (Camera Serial Interface) port of the Raspberry Pi, reducing reliance on extra hubs and ptentially minimizing issues caused by snagging cable.

2. Compact & cost-effective design

    1. The guider and the control computer are integrated into a single form factor.
    2. The system is designed to be budget-friendly, using widely available components while delivering performance at par with commercial astro-computers.

3. Future expandability

    • Planned support for 12V DC power ports to power accessories directly from the guider unit.
    • Modular design to add or swap sensors and cameras as needed.

4. Dual use: astrophotography & visual observing

    • Provides GoTo mount control for telescope pointing.
    • Can act as a “single box” solution whether you’re observing visually or imaging.

## INDIGO Sky with ccd RPi

RaspberryPI image with a pre-configured INDIGO server. This version of OS comes bundled with CCD RPi driver along with the stock drivers that come with the original INDIGO Sky OS.

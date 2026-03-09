# Project Documentation

Welcome to the project documentation.

This documentation is organized into hardware, firmware, and RF design
sections so the project can be understood from board bring-up through
calibration and theory.

## Quick Start

- Read the project overview.
- Build and flash the firmware.
- Review the hardware bring-up procedure.
- Follow the RF calibration process.

## Project Areas

- **Getting Started** covers setup, firmware build, and flashing.
- **Hardware** covers the schematic, PCB layout, bill of materials, and
  bring-up.
- **Firmware** covers software architecture and configuration.
- **RF Design** covers filters, dummy load behavior, detector design, and
  calibration.

## Documentation Assets

Add exported schematic images to `docs/images/schematic/`, PCB screenshots
to `docs/images/pcb/`, measurement plots to `docs/images/measurements/`,
and block diagrams to `docs/images/diagrams/`.

```{toctree}
:maxdepth: 2
:caption: Getting Started

getting_started/overview
getting_started/build_firmware
getting_started/flashing
```

```{toctree}
:maxdepth: 2
:caption: Hardware

hardware/overview
hardware/schematic
hardware/pcb_layout
hardware/bom
hardware/bringup
```

```{toctree}
:maxdepth: 2
:caption: Firmware

firmware/overview
firmware/architecture
firmware/configuration
firmware/api
```

```{toctree}
:maxdepth: 2
:caption: RF Design

rf/overview
rf/filters
rf/dummy_load
rf/detector
rf/calibration
```

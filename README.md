# Orca One V1.0

Orca One is a custom single-board computer built around the Allwinner V3s system-on-chip. This repository contains the editable hardware design, bill of materials, fabrication outputs, and board bring-up documentation.

> **Project status:** Early hardware revision. The design and fabrication files are provided for review and bring-up and have not yet been documented as production-ready.

## Board renders

### Front

![Orca One V1.0 front render](images/orca-one-front.png)

### Back

![Orca One V1.0 back render](images/orca-one-back.png)

## Schematic overview

| Power input | Power rails |
| --- | --- |
| ![USB-C power input schematic](images/schematic-usb-c-power.png) | ![Power rail schematic](images/schematic-power-rails.png) |
| **USB-A 2.0** | **MicroSD card** |
| ![USB-A schematic](images/schematic-usb-a.png) | ![MicroSD card schematic](images/schematic-sd-card.png) |
| **Ethernet** | **Decoupling and bulk capacitors** |
| ![Ethernet schematic](images/schematic-ethernet.png) | ![Decoupling capacitor schematic](images/schematic-decoupling.png) |
| **Expansion and debug headers** | **Allwinner V3s** |
| ![Fan, UART, and GPIO header schematic](images/schematic-headers.png) | ![Allwinner V3s schematic](images/schematic-allwinner-v3s.png) |

## Repository contents

| Path | Contents |
| --- | --- |
| `hardware/kicad/` | KiCad 9 project, schematic, and four-layer PCB layout |
| `hardware/footprints/` | Custom Allwinner V3s LQFP-128 footprint |
| `bom/` | Bill of materials in CSV and XLSX formats |
| `manufacturing/` | Gerber/drill archive and component placement data |
| `images/` | Board photographs and renders |

## Opening the design

1. Install KiCad 9 or a compatible newer release.
2. Open `hardware/kicad/ORCA First Linux Board.kicad_pro`.
3. The project-local footprint table maps the included `v3s` footprint library automatically.

The PCB currently references three optional component STEP models from the original designer's local computer, including the V3s processor and Ethernet connector models. They are not included, so KiCad may show those packages without 3D bodies until redistributable models are added.

## Manufacturing warning

Review the schematic, PCB, BOM, placement data, and fabrication outputs carefully before ordering or assembling boards. Manufacturing outputs may become stale as the editable design changes.

## License

No hardware or documentation license has been selected yet. Unless and until a license file is added, the design remains subject to the repository owner's default copyright rights.

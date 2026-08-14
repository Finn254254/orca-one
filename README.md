<div align="center">

# Orca One V1.0

### A custom Allwinner V3s single-board computer

Hardware design · PCB layout · Manufacturing files · Bring-up documentation

</div>

> [!IMPORTANT]
> **Proprietary design — all rights reserved.** The files are public for viewing and evaluation only. No permission is granted to manufacture, copy, modify, redistribute, or sell this design. See the [license](LICENSE) for the complete terms.

> [!WARNING]
> **Early hardware revision.** The design and fabrication files have not yet been documented as production-ready.

## Board renders

| Front | Back |
| :---: | :---: |
| <img src="images/orca-one-front.png" alt="Orca One V1.0 front render" width="420"> | <img src="images/orca-one-back.png" alt="Orca One V1.0 back render" width="420"> |

## Design overview

The complete editable schematic is included in the KiCad project. Expand a section below for a quick visual tour.

<details>
<summary><strong>Power system</strong> — USB-C input and regulated power rails</summary>

### USB-C power input

![USB-C power input schematic](images/schematic-usb-c-power.png)

### Regulated power rails

![Power rail schematic](images/schematic-power-rails.png)

</details>

<details>
<summary><strong>External interfaces</strong> — USB-A, MicroSD, and Ethernet</summary>

### USB-A 2.0

![USB-A schematic](images/schematic-usb-a.png)

### MicroSD card

![MicroSD card schematic](images/schematic-sd-card.png)

### Ethernet

![Ethernet schematic](images/schematic-ethernet.png)

</details>

<details>
<summary><strong>Processor and supporting circuitry</strong> — Allwinner V3s and decoupling</summary>

### Allwinner V3s

![Allwinner V3s schematic](images/schematic-allwinner-v3s.png)

### Decoupling and bulk capacitors

![Decoupling capacitor schematic](images/schematic-decoupling.png)

</details>

<details>
<summary><strong>Expansion and debug</strong> — fan, UART, and GPIO headers</summary>

![Fan, UART, and GPIO header schematic](images/schematic-headers.png)

</details>

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

Copyright © 2026 Finn Mather. All rights reserved. This is **not an open-source hardware project**. See [LICENSE](LICENSE) for the complete proprietary terms and instructions for requesting permission.

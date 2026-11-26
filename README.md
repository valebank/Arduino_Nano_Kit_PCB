# Arduino Nano Evaluation Kit – PCB

Evaluation board designed in **Altium Designer** around an **Arduino Nano**. It brings together the most common peripherals for learning and prototyping: a 16x2 character LCD, an analog joystick, six LEDs, a relay output and a Bluetooth module.

> Project for *Sistemas de Representación*, Electronic Engineering, UTN.BA (2022).

---

## Features

- **Arduino Nano** (ATmega328P) mounted on female headers, so it can be removed and reused.
- **16x2 LCD** (Winstar WH1602B) driven through its 8-bit parallel interface (`DB0–DB7`, `RS`, `E`).
- **Analog joystick** (COM-09032) with X and Y axes on analog inputs and a push switch.
- **6 indicator LEDs**, each with its current limiting resistor.
- **Relay output** (SRD series) driven by a BC817-25 NPN transistor, with a 1N4148 flyback diode and a 3-way pluggable terminal block for the load.
- **HC-05 Bluetooth module** connected to the Nano's serial port (`TxD`/`RxD`).
- **DC power jack** (PJ-002BH) feeding the Nano `VIN` input.

## Schematic structure

The design is hierarchical: a top-level block diagram sheet links three functional sheets.

| Sheet | Content |
|---|---|
| `KIT_ARDUINO_BLK_R00.SchDoc` | Block diagram: connects the CPU, communication and peripheral sheets |
| `KIT_ARDUINO_CPU_R00.SchDoc` | Arduino Nano, female headers and power jack |
| `KIT_ARDUINO_COM_R00.SchDoc` | HC-05 Bluetooth module on the serial port |
| `KIT_ARDUINO_PER_R00.SchDoc` | LCD, joystick, LEDs and relay driver |

## PCB

- 2-layer board (top and bottom copper).
- Mixed technology: SMD passives and semiconductors (0805 resistors, SOT-23 transistor, SOD-323 diode) together with through-hole connectors, LEDs and modules.
- Custom footprints for the LCD, joystick, relay, terminal block, Bluetooth header and power jack.
- **Assembly variant** defined in the project (`KIT_ARDUINO_ConVariante_R00.PrjPcb`), with its bill of materials (`.BomDoc`).

## Repository contents

| File | Description |
|---|---|
| `KIT_ARDUINO_ConVariante_R00.PrjPcb` | Altium project (open this file) |
| `*.SchDoc` | Schematic sheets |
| `KIT_ARDUINO_R00.PcbDoc` | PCB layout |
| `KIT_ARDUINO_R00.SchLib`, `KIT_ARDUINO_R00.PcbLib`, `PowerJack_THT_R00.PcbLib` | Custom symbol and footprint libraries |
| `KIT_ARDUINO_ConVariante_R00.BomDoc` | Bill of materials |

## Opening the project

Open `KIT_ARDUINO_ConVariante_R00.PrjPcb` in Altium Designer. The schematics and the PCB open from the *Projects* panel; press `3` in the PCB editor to see the 3D view.

## Tools

Altium Designer · Hierarchical schematic design · 2-layer PCB layout · Custom symbol and footprint libraries · Assembly variants · Bill of materials

## Author

[Valeria Bank](https://www.linkedin.com/in/valeria-bank-324197200/)

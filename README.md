# LDR Light-Activated Switch Using KiCad

## Project Overview

This project presents the schematic design and PCB layout of a **6 V DC LDR Light-Activated Switch** developed using KiCad. The circuit uses a Light Dependent Resistor (LDR) to detect ambient light and an NPN BC547 transistor to control an LED automatically.

The project covers circuit schematic design, component footprint assignment, PCB layout, Design Rule Checking (DRC), and Gerber and drill file generation.

## Objectives

- Design a light-sensitive switching circuit.
- Understand LDR-based voltage dividers.
- Use an NPN transistor as an electronic switch.
- Design a PCB using KiCad.
- Generate manufacturing files for PCB fabrication.

## Components Used

| Component | Value / Description | Quantity |
|---|---|---:|
| J1 | 2-pin, 6 V DC input connector | 1 |
| R1 | 10 kΩ resistor | 1 |
| R2 | 470 Ω resistor | 1 |
| R3 | Light Dependent Resistor (LDR) | 1 |
| R4 | 10 kΩ resistor | 1 |
| Q1 | BC547 NPN transistor | 1 |
| D1 | LED | 1 |

## Tools Used

- **KiCad** — Schematic capture and PCB design
- **PCB Editor** — Component placement and copper routing
- **DRC** — PCB design rule verification
- **Gerber Viewer** — Manufacturing file inspection

## Working Principle

The LDR changes its resistance according to the intensity of the light falling on it. Together with R1, it forms a voltage divider that produces a light-dependent voltage at the `LIGHT_SENSE` node.

The BC547 transistor receives this signal through R4 and operates as a switch. The LED is connected to the 6 V supply through a 470 Ω current-limiting resistor.

- **Bright light:** The LDR resistance decreases, raising the voltage at `LIGHT_SENSE`. The transistor turns on, and the LED lights up.
- **Low light or darkness:** The LDR resistance increases, lowering the voltage at `LIGHT_SENSE`. The transistor turns off, and the LED goes off.

*Note: The actual switching threshold depends on the LDR characteristics and the selected resistor values. The circuit should be tested to confirm its behavior.*

## Design Workflow

1. Created the circuit schematic in KiCad.
2. Connected the power supply, LDR voltage divider, transistor switch, and LED output.
3. Assigned component footprints.
4. Transferred the schematic to PCB Editor.
5. Arranged the components and routed the copper tracks.
6. Ran the Design Rule Checker (DRC).
7. Generated Gerber and drill files for manufacturing.

## PCB Design Verification

- Schematic Electrical Rules Check (ERC) completed.
- PCB Design Rule Check (DRC) reported zero errors.
- Gerber and drill files generated.

Zero DRC errors do not independently guarantee electrical correctness. Component pin mapping, connector polarity, LED orientation, and manufacturing files must also be verified before fabrication.

## Applications

- Automatic light-sensitive indicators
- Basic light-detection circuits
- Electronics learning and prototyping
- Introductory PCB design practice

## Future Improvements

- Add an adjustable light-sensitivity threshold.
- Replace the fixed switching threshold with a comparator circuit.
- Add a relay or MOSFET output stage for suitable external loads.
- Assemble and test the fabricated PCB under different lighting conditions.

## Learning Outcomes

This project provided practical experience with analog sensor interfacing, voltage-divider circuits, transistor switching, schematic capture, footprint assignment, PCB routing, DRC, and manufacturing file generation.

## Author

**Divakar R**  
B.E. Electronics and Communication Engineering  
Adithya Institute of Technology, Coimbatore, Tamil Nadu, India

## License

This project is intended for educational and prototyping purposes. A formal license can be added if the design is distributed or reused publicly.

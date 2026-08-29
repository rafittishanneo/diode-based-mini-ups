# Diode-Based Mini UPS

A university Electronic Devices project demonstrating an automatic DC power backup system using diodes, a capacitor, a 12V main power supply, and a 9V backup battery.

## Overview

This project implements a simple mini UPS circuit that automatically switches between a primary DC power source and a backup battery.

The circuit uses two 1N4007 diodes to prevent reverse current and select the available power source. A 1000µF capacitor provides short-term energy storage and helps produce a smooth transition when the main power supply is disconnected.

## Objectives

- Demonstrate the one-way operation of a diode.
- Design an automatic DC power source selection circuit.
- Prevent reverse current between the main supply and backup battery.
- Study the role of a capacitor in temporary power backup.
- Compare theoretical calculations with Multisim simulation results.

## Circuit Components

| Component | Specification | Quantity |
|---|---:|---:|
| DC power supply | 12V | 1 |
| Backup battery | 9V | 1 |
| Diode | 1N4007 | 2 |
| Electrolytic capacitor | 1000µF | 1 |
| LED | 5mm | 1 |
| Connecting wires | - | As required |
| Simulation software | Multisim | 1 |

## Working Principle

The circuit has two operating modes:

### Normal Mode

When the 12V main supply is available, the first diode conducts and supplies power to the load. The capacitor is also charged.

The approximate output voltage is:

```text
Output voltage = 12V - 0.7V = 11.3V
```

The backup battery diode remains reverse-biased, so the battery does not supply current.

### Backup Mode

When the main supply is disconnected, the backup source supplies the load through the second diode. The capacitor helps maintain the output during the transition.

The approximate output voltage is:

```text
Output voltage = 9V - 0.7V = 8.3V
```

## Results

| Operating mode | Output voltage | Theoretical battery current | Simulation battery current |
|---|---:|---:|---:|
| 12V main supply ON | 11.3V | 0mA | 3.55µA |
| 9V backup battery ON | 8.3V | 9.7mA | 9.7588mA |

The simulation results were close to the theoretical calculations.

## Advantages

- Simple and inexpensive design.
- Automatic source switching.
- Prevents reverse current.
- Easy to construct and simulate.
- Useful for understanding basic power backup systems.

## Limitations

- The diode voltage drop reduces efficiency.
- The circuit does not include a battery charging system.
- Output voltage may fluctuate under higher loads.
- A basic 9V battery is not ideal for long-term high-current backup.
- The circuit is not suitable for sensitive devices without additional regulation.

## Future Improvements

- Add a battery charging circuit.
- Replace the diodes with MOSFET-based ideal-diode switching.
- Use a rechargeable battery.
- Add a voltage regulator.
- Use a larger capacitor for longer transition support.
- Add protection against overcharging, short circuits, and deep discharge.
- Test the circuit with different loads.

## Simulation

The circuit was designed and tested using Multisim. Simulation files and screenshots are available in the `circuit/` directory.

## Project Documentation

Project presentation and report:

- [Project Presentation](docs/project-presentation.pptx)
- [Project Report](docs/project-report.pdf)

## Academic Information

- Course: Electronic Devices
- Project: Mini UPS Demonstration Using Diodes
- Group: Group 4
- Institution: Add your university name here
- Semester: Add your semester here
- Academic year: Add the academic year here

## Safety Notice

This project is intended for low-voltage DC experimentation. Do not connect the circuit directly to AC mains electricity. Check the polarity of the electrolytic capacitor and battery before powering the circuit.

## License

This project is available for educational and academic purposes under the MIT License.

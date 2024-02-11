## Overview

The LV2841 and LV2842 are PWM DC/DC buck (stepdown) regulators. With a wide input range from 4V-40V, they are suitable for a wide range of application from industrial to automotive for power conditioning from unregulated source.

![LV2842](https://firebasestorage.googleapis.com/v0/b/atopile.appspot.com/o/lv2842xlvddcr.png?alt=media&token=5e136803-662d-49ba-821d-12c19738b427 "LV2842")

## Usage Example

```
import LV2842 from "lv2842/lv2842.ato"
import Power from "generics/interfaces.ato"

module BuckRegulatorCircuit:
   inputPower = new Power
   buckRegulator = new LV2842
   
   # Configure input power interface for buck regulator
   inputPower.voltage = "4V to 40V"  # Wide input voltage range
   
   # Connect input power to buck regulator
   buckRegulator.vin ~ inputPower.vcc
   
   # Optional: Set output voltage and other parameters as needed
   buckRegulator.vout = "3.3V"  # Example output voltage
   buckRegulator.enable = true  # Enable the regulator

```

## Features

### Input Voltage Range: 
4V to 40V, suitable for industrial and automotive applications.

### Output Voltage: 
Configurable based on the requirements of the regulated power supply.

### Regulation: 
PWM control for efficient step-down voltage regulation.

## Contributing
Contribute to this package using pull requests.

## License
This current-sense amplifier module is provided under the MIT License.

## Contact
For further inquiries or support, please contact me at narayan@atopile.io.





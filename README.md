## Overview
This repository is the central hub for the **Powder Dispenser and Weighing Module** project. It combines both hardware and software components to deliver a comprehensive solution for precise powder dispensing and measurement. The project has been modularized into separate repositories for hardware and software, making it easier to manage, develop, and contribute to specific aspects independently.

### Key Features:
- **Modular Design**: Separate hardware and software repositories ensure clear organization and enable independent development.
- **Precise Control**: The system integrates advanced software and firmware to ensure high precision in powder dispensing and weighing.
- **Open Source**: Hardware and software are released under open-source licenses, encouraging collaboration and community contributions.

## Repository Structure
This repository primarily links to its two submodules:

### **[hardware](https://github.com/loppe35/PowderDispenser_BuildFiles.git)**
- Contains all hardware-related files, including:
  - 3D models (STL and STEP files) for prototyping and manufacturing.
  - Circuit schematics and layouts.
  - Assembly instructions.
- Licensed under the **CERN Open Hardware License v2.0 (OHL-W)**.

### **[software](https://github.com/loppe35/PowderDispenser_FWSW.git)**
- Includes software and firmware components:
  - Source code and libraries for hardware control.
  - Configuration files for customizing the system.
  - Test scripts and Jupyter notebooks for data analysis.
- Licensed under the **MIT License**.

## Getting Started
To get started with this project, clone the repository along with its submodules:

```bash
# Clone the main repository with submodules
git clone --recurse-submodules https://github.com/loppe35/PowderDispensing_and_Weighing_Module.git
```

### Workflow
A typical workflow involves the following steps:
1. **Set Up Hardware**:
   - Print 3D parts using STL files from the BuildFiles repository.
   - Assemble components following the BuildFiles repository guide.
   - Connect hardware as per the wiring diagrams.
2. **Flash Firmware**:
   - Compile and upload firmware using the software repository's `PowderDispenserCPP` directory.
3. **Configure System**:
   - Edit `config.json` for your specific hardware and operational requirements.
4. **Run System**:
   - Use Jupyter notebooks in the software repository for testing, calibration, and dispensing operations.

### Hardware Setup
1. **3D Printing**: Use the STL files in the hardware submodule to print the necessary parts.
2. **Assembly**: Follow the detailed assembly instructions and schematics provided in the hardware documentation.
3. **Circuit Integration**: Connect the hardware components as specified in the wiring diagram referred to in the hardware repository.

### Software Setup
1. **Install Dependencies**:
   - Navigate to the directory in the software submodule.
      - It is recommended to create a virtual environment
   - Run the following command to install Python dependencies:
     ```bash
     pip install -r requirements.txt
     ```
2. **Compile Firmware**:
   - Use the provided C++ files in the `PowderDispenserCPP` directory to compile and upload the firmware to the Arduino.
3. **Configure System**:
   - Edit the `config.json` file to match your specific hardware and operational parameters.

## Documentation
Comprehensive documentation is available in the README of each submodule. This includes:
- **Hardware Designs**: File descriptions, usage instructions, and examples for modification.
- **Software Details**: Step-by-step installation guides, usage instructions, and code documentation.
- **Examples and Results**: Demonstrations of typical use cases with expected outcomes.

## Licenses
This project follows a dual licensing structure:

1. **Hardware**:
   - Licensed under the **CERN Open Hardware License v2.0 (OHL-W)**.
   - Allows for modification, distribution, and commercial use under the terms of the license.
2. **Software**:
   - Licensed under the **MIT License**.
   - Permits free use, modification, and distribution with minimal restrictions.

Refer to the `LICENSE` files in each submodule for detailed licensing terms.

## Troubleshooting
### Common Issues:
1. **Hardware Not Detected**:
   - Ensure the microcontroller is connected to the correct port.
   - Run the `list_serial_ports` function in the FWSW repository to verify the connection.
2. **Weight Measurements Inconsistent**:
   - Check the load cell connections and ensure they are properly secured.
   - Verify the calibration settings in `config.json`.
3. **Stepper Motor Not Responding**:
   - Verify the wiring and power supply to the motor.
   - Check the motor driver connections.

## Contributing
Contributions are vital for the growth and success of this project. Whether you are improving the design, optimizing the software, or testing the system, your input is highly appreciated.

### Guidelines:
- Ensure compliance with the licensing terms for hardware and software contributions.
- Follow the code of conduct and adhere to the contribution guidelines provided in the submodules.
- Submit pull requests with detailed explanations of changes.

## Future Improvements
- **Integration with DOI**: A DOI link will be added once available, providing a permanent reference for citation and academic use.

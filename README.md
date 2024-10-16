# Hall Sensor Monitor

**Hall Sensor Monitor** is a LabVIEW-based application for reading and processing data from a Hall effect sensor connected to an analog input channel of a DAQ device. The program allows users to measure magnetic field strength in milliteslas (mT) and display the results in real-time. Additionally, it includes control logic for switching between different operational modes based on user input.

## Features:
- **Analog Input**: Reads data from a connected Hall effect sensor via the `Dev1/ai0` channel.
- **Magnetic Field Calculation**: The program processes the raw voltage signal from the sensor and converts it into a magnetic field strength measurement in milliteslas (mT).
- **GUI Controls**: Simple user interface allowing the user to switch between different operational modes.
- **Real-Time Monitoring**: The measured magnetic field is displayed in real-time.

## How It Works:
1. **Channel Configuration**:
   - The program reads the analog voltage signal from channel `Dev1/ai0` where the Hall effect sensor is connected.
   - The raw voltage is converted to a magnetic field strength in milliteslas (mT) using a scaling factor.

2. **Operational Modes**:
   - The program allows the user to switch between different modes using a dropdown menu in the GUI.
   - Available modes include:
     - `"def"`: Default mode, which continues normal operation.
     - `"A1"`: Active mode 1, where specific processing or behavior is applied to the input.
     - `"Exit"`: Terminates the program.

3. **Data Processing**:
   - The voltage input from the Hall effect sensor is processed and scaled using a linear formula.
   - The result is displayed in milliteslas, providing real-time feedback about the magnetic field strength.

4. **Graphical User Interface (GUI)**:
   - Users can interact with the program through the GUI, choosing the operational mode and viewing the real-time magnetic field measurements.
   - The system continuously updates the measurement display unless the user selects the "Exit" option to terminate the program.

## Requirements:
- **Hardware**: NI DAQ device with an analog input channel connected to a Hall effect sensor.
- **Software**: LabVIEW with NI-DAQmx drivers installed.

## Usage:
1. Connect the Hall effect sensor to the appropriate analog input channel (`Dev1/ai0`).
2. Run the program in LabVIEW.
3. Use the GUI to select the desired operational mode.
   - In default mode, the system will continuously monitor and display the magnetic field in real-time.
4. To stop the program, select the "Exit" option in the GUI.

## Example:
- The user connects a Hall effect sensor to channel `Dev1/ai0`.
- After running the program, the user can observe the real-time magnetic field readings, which are scaled from the voltage input of the sensor.
- The system continues to monitor the magnetic field until the user selects "Exit" from the mode options.

## Troubleshooting:
- Ensure the Hall effect sensor is properly connected to the DAQ device.
- Verify that the DAQmx drivers are installed and configured correctly.
- If measurements appear incorrect, check the scaling factor in the voltage-to-millitesla conversion process.

## Code:
![image](https://github.com/user-attachments/assets/9991a11f-10a0-49a3-9e80-7835e256823d)

## Program view:
![image](https://github.com/user-attachments/assets/f40a4a91-dcdb-4633-a37a-bdc9e39a1296)

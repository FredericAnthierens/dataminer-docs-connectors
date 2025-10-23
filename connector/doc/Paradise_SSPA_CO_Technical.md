---
uid: Connector_help_Paradise_SSPA_CO_Technical
---

# Paradise SSPA CO

## About

This connector is used to monitor and control compact outdoor solid-state power amplifiers (SSPAs) via serial communication. It provides visibility on amplifier performance, electrical readings, and fault indicators, and allows configuration of system behavior and alarm thresholds.

## Configuration

### Connections

#### Serial connection

This connector uses a serial connection and requires the following input during element creation:

- **Type of port**: The type of port of the connection. By default: *TCP/IP*.
- **IP address/host**: The polling IP or URL of the destination, e.g. *10.245.83.199*.
- **IP port**: The port of the destination, e.g. *7008*.
- **Bus address**: The bus address of the connected device, e.g. *1*.

## Usage

### System Info

The following system info parameters are shown:

- RF Power Level
- Reflected RF Power
- Present Attenuation Level
- SSPA Current
- Power Supply Voltage
- Temperature

### Communication Info

The following communication configuration parameters are shown:

- Protocol Select
- Baudrate
- Network Address

### Fault Status

The following key fault indicator status information is shown:

- Summary Fault
- High Temperature Fault
- Low DC Voltage Fault
- Low DC Current Fault
- BUC Fault
- Auxiliary and Spare Faults
- RF Switch 1 and 2 State
- Unit Online Status

### Fault Monitoring Setup

The following alarm thresholds and logic configuration is possible:

- Fault Logic (BUC, Spare, Auxiliary)
- Handling settings per fault type
- Thresholds for high temperature, low current, and spare fault window
- Normalize RF Power Level

### System Setup

The following parameters allow basic device control and configuration:

- Attenuation Level
- Standby Mode
- Mute State
- Gain Control Authority
- SSPA Calibration Mode
- System Mode
- Unit Startup State
- System Hierarchical Address

## Notes

The connector was tested using firmware version **3.53** of the SSPA.

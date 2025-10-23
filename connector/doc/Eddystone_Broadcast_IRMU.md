---
uid: Connector_help_Eddystone_Broadcast_IRMU
---

# Eddystone Broadcast RMU

The Eddystone Broadcast RMU enabled FM transmitters can enable your network operations center and authenticated engineers to remotely view and manage any transmitter system.

## About

### Product Info

| Range     | Supported Firmware     |
|-----------|------------------------|
| 1.0.0.x   | 4.0.4612.24969         |
| 1.0.1.x   | 4.0.4612.24969         |
| 1.1.0.x   | 5.6.7310.16328         |

## Configuration

### Connections

#### SNMP main connection

This connector uses an SNMPv1 connection and requires the following input during element creation:

SNMP CONNECTION:

- **IP address/host**: The polling IP of the device.

SNMPv1 Settings (1.0.0.x):

- **Port number**: The port of the connected device, by default *161*.
- **Get community string**: The community string used when reading values from the device, by default *public*.
- **Set community string**: The community string used when setting values on the device, by default *private*.

### Web Interface

The web interface is only accessible when the client machine has network access to the product.

## How to use (1.0.0.x)

The element created with this connector consists of the following data pages:

- **General**: Displays general **system information** as well as the IRMU **device information**. Also allows you to configure general **device settings**.
- **Inputs/Outputs/Sensors/Exciters/Amplifiers/Triggers**: These pages contain information about the Boolean inputs, Boolean outputs, sensors, exciters, transmitters, amplifiers, and triggers, respectively
- **Web Interface**: Displays the web interface of the polling IP address.

---
uid: Connector_help_Supermicro_X9DRW_Technical
---

# Supermicro X9DRW Connector

## About

The Supermicro X9DRW connector is designed to interface with the Supermicro server. It collects and visualizes device and sensor metrics via SNMP.

## Configuration

### Connections

#### SNMP Connection

This connector uses a Simple Network Management Protocol (SNMP) connection and requires the following input during element creation:

SNMP CONNECTION:

- **IP address/host**: The IP address of the Moxa NPort device.
- **Device address**: Not required.

SNMP Settings:

- **Port number**: 161 (default).

### Web Interface

The web interface is only accessible when the client machine has network access to the product.

## How to Use

In the element, the SNMP parameters polled by the connector are shown on different data pages:

- **General**: System description parameters.
- **Sensor**: Sensor values for temperature, voltage, power, battery, and PSU.
- **FAN**: FAN details for 6 FANs that are used by device.
- **Web Interface**: The web UI of the device.

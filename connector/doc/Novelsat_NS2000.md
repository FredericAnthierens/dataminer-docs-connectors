---
uid: Connector_help_Novelsat_NS2000
---

# Novelsat NS2000

The NovelSat NS2000 is a demodulator designed for high-demand satellite reception. The NS2000 delivers significantly higher spectral efficiency compared to DVB-S2.

## About

This connector uses **SNMP and HTTP** communication to monitor and change parameters on the device, to guarantee the efficiency of the equipment.

### Version Info

| Range              | Description                          | DCF Integration | Cassandra Compliant |
|--------------------|--------------------------------------|-----------------|---------------------|
| 1.0.0.x            | Initial version.                     | No              | Yes                 |
| 1.0.1.x            | Added DCF integration.               | Yes             | Yes                 |
| 1.0.2.x            | Monitor Alarm Table with Naming.     | Yes             | Yes                 |
| 2.0.0.x            | Added HTTP connection.               | Yes             | Yes                 |
| 2.1.0.x [Obsolete] | New firmware based on 2.0.0.x.       | Yes             | Yes                 |
| 2.1.1.x [SLC Main] | Changes implemented to display keys. | Yes             | Yes                 |

### Product Info

| Range   | Supported Firmware Version |
|---------|----------------------------|
| 2.1.1.x | 1.1.1 [Build 4761]         |

## Configuration

### Connections - 1.0.0.x/1.0.1.x/1.0.2.x

#### SNMP Main Connection

This connector uses a Simple Network Management Protocol (SNMP) connection and requires the following input during element creation:

SNMP CONNECTION:

- **IP address/host**: The polling IP of the device.

SNMP Settings:

- **IP port**: The IP port of the device (default: *161*).
- **Get community string**: The community string used when reading values from the device (default: *public*).
- **Set community string**: The community string used when setting values on the device (default: *private*).

### Connections - 2.0.0.x/2.0.1.x/2.1.1.x

#### SNMP Main Connection

This connector uses a Simple Network Management Protocol (SNMP) connection and requires the following input during element creation:

SNMP CONNECTION:

- **IP address/host**: The polling IP of the device.

SNMP Settings:

- **IP port**: The IP port of the device (default: *161*).
- **Get community string**: The community string used when reading values from the device (default: *public*).
- **Set community string**: The community string used when setting values on the device (default: *private*).

#### HTTP Secondary Connection

This connector uses an HTTP connection and requires the following input during element creation:

HTTP CONNECTION:

- **IP address/host**: The polling IP of the device.
- **IP port**: The IP port of the device.
- **Device address**: The device address (default: *BypassProxy*).

### Firmware Configuration

When the element has been created, specify the correct device firmware on the System page. This value can be saved, so that you do not need to specify it again if the element is restarted or stopped.

## Usage

### System

This page contains general information related to the device, such as the **Firmware Version**, **OS Version** and **HW Product Type.**

In the **Firmware Device** box, you can select the firmware version of the device. The correct firmware version must be selected in order to ensure that the connector functions correctly.

### System Config

On this page, you can configure the device, for example with the **DHCP** toggle button, the **Serial Port** settings and the **Clock Source** toggle button.

There is also a **page button** that allows you to modify the date and time of the device.

### Line Config

This page contains demodulator settings, including **Line Mode**, **RF Frequency**, **LNB Control**, **ACM Mode** and **Symbol Rate.**

### Channel Config

This page contains demodulator channel settings. For both channels, you can check and configure the **Range From** and **Range to**.

### Interface Config

This page contains three tables with demodulator interface information (Test, ASI and Ethernet). You can configure various parameters, such as **DIT Source**, **DIA Data Rate** and **DEI Source.**

### Line Monitoring

This page allows you to monitor demodulator information and provides a detailed overview of the configuration of the demodulator.

### Channel Monitoring

This page contains the **Demodulator Line Channel Table**.

### Interface Monitoring

This page contains demodulator interface information.

### Alarm / Event Monitoring

This page contains two tables with alarms and events of the demodulator, respectively.

The **Monitor Alarm Table** provides an overview of alarm information for the device. The **Monitor Events Table** takes approximately 2 minutes to be polled. Polling for this table can be disabled with the **Poll Monitor Events** toggle button. You can also poll the table on demand with the **Refresh Events** button.

### System Monitoring

This page contains information such as the **FPGA Temperature**, **System Board Temperature** and **Type of Clock Source**.

### DRM

This page contains DRM information: **System DRM Private Key Table**, **System DRM Remotes AES Table**, **System DRM Local AES Table**, **System DRM Activate Key AES Table** and **System DRM Entitlement Table**.

### Web Interface

This page provides access to the web interface of the device (http:// Port 80). This may require access credentials (user name/password). Note that the client machine has to be able to access the device, as otherwise it will not be possible to open the web interface.

## DataMiner Connectivity Framework

The 2.1.1.x connector range of the connector supports the usage of DCF.

### Interfaces

#### Fixed interfaces

Virtual fixed interfaces:

- L-band (in)
- ASI1 (out)
- AS2 (out)

### Connections

#### Internal Connections

- Between L-Band and ASI1
- Between L-Band and ASI2

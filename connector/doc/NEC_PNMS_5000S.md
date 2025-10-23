---
uid: Connector_help_NEC_PNMS_5000S
---

# NEC PNMS 5000S

This connector processes traps received from the NEC PMNS 5000S system.

## About

This connector can receive and process **traps** sent from the NEC PNMS 5000S system.

### Version Info

| Range                | Key Features     | Based on     | System Impact     |
|----------------------|------------------|--------------|-------------------|
| 1.0.1.x [SLC Main]   | Initial version  | -            | -                 |

### Product Info

| Range     | Supported Firmware     |
|-----------|------------------------|
| 1.0.1.x   | -                      |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 1.0.1.x   | Yes                 | Yes                     | -                     | -                       |

## Installation and configuration

### Creation

#### SNMP Main Connection

This connector uses a Simple Network Management Protocol (SNMP) connection and requires the following input during element creation:

SNMP CONNECTION:

- **IP address/host**: The polling IP of the NEC PNMS 5000S system.
- **Device address**: The IP address of the corresponding network element. This IP will be used to filter the traps.

SNMP Settings:

- **IP port**: The IP port of the device.

## Usage

### LMS Alarm and Status

This page displays all LMS alarms and statuses.

There are two page buttons with extra information regarding **External Do** and **External Di**.

The **Clear Trap Data** button can be used to clear the alarms received via traps from the device.

### SWO PROC & SYS Group

This page displays all SWO PROC & SYS Group alarms and statuses.

Each row contains a **Clear Alarms** button that can be used to clear the alarms received via traps from the device for that particular row.

### Remote DCF Interface Table

This page displays the **Remote DCF Interface Table.**

## DataMiner Connectivity Framework

The **1.0.1.1** connector range of the NEC PNMS 5000S connector supports the usage of DCF.

DCF can also be implemented through the DataMiner DCF user interface and through DataMiner third-party connectors (for instance a manager).

### Interfaces

#### Fixed interfaces

Physical fixed interfaces::

- **Eth1**: inout type
- **Eth2**: inout type

#### Dynamic Interfaces

Physical dynamic interfaces:

For each row in the **SYS Group Alarm And Status** table, two interfaces are created:

- **INOUT**: inout type
- **MW0**: inout type

### Connections

#### Internal Connections

- For each row in the **SYS Group Alarm And Status** table, two interfaces are created that are connected to each other.

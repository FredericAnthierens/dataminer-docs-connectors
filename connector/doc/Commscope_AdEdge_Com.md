---
uid: Connector_help_Commscope_AdEdge_Com
---

# Commscope AdEdge Com

This SNMP connector allows the user to monitor the Commscope AdEdge Com device. Its main feature is its alarm information.

## About

### Version Info

| Range                | Key Features     | Based on     | System Impact     |
|----------------------|------------------|--------------|-------------------|
| 1.0.0.x [SLC Main]   | Initial version  | -            | -                 |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 1.0.0.x   | No                  | Yes                     | -                     | -                       |

## Configuration

### Connections

#### SNMP Main Connection

This connector uses a Simple Network Management Protocol (SNMP) connection and requires the following input during element creation:

SNMP CONNECTION:

- **IP address/host**: The polling IP or URL of the destination.
- **IP port**: The IP port of the destination.

SNMP Settings:

- **Get community string**: The community string used when reading values from the device (default: *public*).
- **Set community string**: The community string used when setting values on the device (default: *private*).

### Web Interface

The web interface is only accessible when the client machine has network access to the product.

## How to use

The **General** page shows **System Info** parameters like **Name**, **Description**, **Model**, and **Uptime**.

The **Alarms** page shows the active alarms as well as the **Alarm Definition**, which is used to map the description when an active alarm is detected.

## Notes

This connector does not perform any sets.

---
uid: Connector_Juniper_Networks_MX_Series_Technical
---

# Juniper Networks MX Series Technical

## About

The Juniper Networks MX Series is a family of Ethernet routers and switches designed for service providers, cloud operators, and large enterprises. These devices support a wide range of networking use cases such as edge routing, core routing, data center interconnect, and enterprise WAN aggregation. This connector is used to monitor and control such MX Series routers.

## Configuration

### Connections

#### SNMP Connection - SNMP Connection

This connector uses a Simple Network Management Protocol (SNMP) connection and requires the following input during element creation:

SNMP CONNECTION:

- **IP address/host**: The polling IP or URL of the destination.

SNMP Settings:

- **Port number**: The port of the connected device, by default 161.
- **Get community string**: The community string used when reading values from the device (default: *public*).
- **Set community string**: The community string used when setting values on the device (default: *private*).

### Web Interface

The web interface is only accessible when the client machine has network access to the product.

## How to Use

The **health** of the different router components such as **Routing Engine**, **PICs**, **Fans**, etc. can be monitored on the **Operation** page.

The basic interface information such as the name, admin and operational states, speed, etc. of the interfaces is displayed on the **Interface** page.

The **Juniper-specific enhancements** of the interfaces are shown on the **Interface Extension**, **Policer**, **Media**, **Traffic**, and **Accounting** pages.

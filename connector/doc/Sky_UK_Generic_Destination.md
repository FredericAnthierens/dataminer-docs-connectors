---
uid: Connector_help_Sky_UK_Generic_Destination
---

# Sky UK Generic Destination

This DataMiner connector can be used to create generic destination resources for SRM.

## About

### Version Info

| Range                | Key Features     | Based on     | System Impact     |
|----------------------|------------------|--------------|-------------------|
| 1.0.0.x [SLC Main]   | Initial version  | -            | -                 |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components                               | Exported Components     |
|-----------|---------------------|-------------------------|-------------------------------------------------|-------------------------|
| 1.0.0.x   | Yes                 | Yes                     | This connector is to be used together with SRM. | -                       |

## Configuration

### Connections

#### Virtual Connection - Main

This connector uses a virtual connection and does not require any input during element creation.

### Initialization

See "How to use".

### Redundancy

There is no redundancy defined.

## How to use

The main goal of this connector is to be able to create generic rows for destinations, which will later on be used by the SRM framework to create resources. These resources will then be used inside bookings.

The **General** page contains the **Destinations Table**. To add or remove rows, use the right-click menu.

## DataMiner Connectivity Framework

The **1.0.0.x** range of the Sky UK Generic Destination connector supports the usage of DCF.

DCF can also be implemented through the DataMiner DCF user interface and through third-party DataMiner connectors (e.g. a manager).

### Interfaces

#### Dynamic interfaces

Virtual dynamic interfaces:

- DCF interfaces (type in) are created for all destination defined in the **Destinations Table**.

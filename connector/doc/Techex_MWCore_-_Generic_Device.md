---
uid: Connector_help_Techex_MWCore_-_Generic_Device
---

# Techex MWCore - Generic Device

This connector is used by Dynamic Virtual Elements (DVEs) exported by the Techex MWCore parent connector.

## About

### Version Info

| Range              | Key Features                              | Based on   | System Impact   |
|----------------------|---------------------------------------------|--------------|-------------------|
| 1.0.0.x [SLC Main]   | Initial version (includes DCF integration). | -            | -                 |

### Product Info

| Range     | Supported Firmware     |
|-----------|------------------------|
| 1.0.0.x   | 5.3.0-alpha.3          |

## Configuration

This connector is automatically created by the parent connector [Techex MWCore](xref:Connector_help_Techex_MWCore).

### Web Interface

The web interface is only accessible when the client machine has network access to the product.

## How to use

The element contains general information, network information and settings for a device monitored by the MWCore platform.

## DataMiner Connectivity Framework

The **1.0.0.x** connector range of the Techex MWCore - Generic Device connector supports the usage of DCF.

DCF can also be implemented through the DataMiner DCF user interface and through DataMiner third-party connectors (for instance a manager).

Connectivity for this protocol is managed by the parent protocol Techex MWCore.

### Interfaces

#### Dynamic interfaces

Virtual dynamic interfaces:

- **Output:** Created to interface with the DVE table with **interface type** **out**.


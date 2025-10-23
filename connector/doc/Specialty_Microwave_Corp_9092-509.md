---
uid: Connector_help_Specialty_Microwave_Corp_9092-509
---

# Specialty Microwave Corp 9092-509

The 9092-509 is a BDC supply and protection switch. It supplies power to four low-noise amplifiers (BDC) and provides redundancy protection switching logic for the BDCs.

This connector allows quick monitoring of the operation states of the device's components. It also allows you to control switch configurations and positions remotely.

## About

### Version Info

| Range              | Key Features                                                                                 | Based on | System Impact |
|--------------------|----------------------------------------------------------------------------------------------|----------|---------------|
| 1.0.0.x [SLC Main] | Initial version: <br>- Monitoring front panel information <br>- Configuring switch positions | -        | -             |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 1.0.0.x   | No                  | Yes                     | -                     | -                       |

## Configuration

### Connections

#### Serial Connection - Main

This connector uses a serial connection and requires the following input during element creation:

SERIAL CONNECTION:

- Interface connection:

  - **IP address/host**: The polling IP or URL of the destination.
  - **IP port**: The IP port of the destination.
  - **Bus address**: The bus address of the device. Default: *49*. Range: *33* - *126*.

## How to use

The **General** page displays all the front panel information. The properties mentioned below can be configured here as well.

Note that the **Control Status** **on the device has to be set to** ***Remote*** for commands from DataMiner to work.

- **Unit Mode**: Can be set to *Auto* or *Manual*. If you want to be able to manually change positions of switches, this mode must be set to *Manual*.

- **Switch Positions**: These can be configured so that the switches are using their main HPA or the standby HPA.

- **Toggle Switch:** Allows you to toggle the switch position with the **Toggle Switch 1** and **Toggle Switch 2** buttons.

- **Unit State**: Sets both switches to specific state at the same time instead of setting them individually.

- *Normal*: Both switches are set to their main HPA.
  - *Backup 1*: Switch 1 is set to BDC Standby and Switch 2 is set to its main BDC.
  - *Backup 2*: Switch 2 is set to BDC Standby and Switch 1 is set to its main BDC.

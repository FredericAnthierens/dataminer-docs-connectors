---
uid: Connector_help_Xicom_Technology_XTC-11x
---

# Xicom Technology XTC-11x

With this connector, you can monitor **Xicom XTC-11x** controllers. It also allows you to poll a number of general fault parameters from each individual HPA connected to the controller.

## About

### Version Info

| Range              | Key Features                                                         | Based on | System Impact |
|--------------------|----------------------------------------------------------------------|----------|---------------|
| 1.0.0.x            | Initial version. Deprecated range.                                   | -        | -             |
| 1.0.1.x            | Removed functionality: HPA-A RF, HPA-B RF, Enable all/Inhibited all. | -        | -             |
| 1.1.1.x            | Removed functionality: PSU 1/PSU 2 Status parameters.                | 1.0.1.x  | -             |
| 1.1.0.x            | Support for 4 switches and minimal faults/alarming per HPA.          | -        | -             |
| 1.2.0.x [SLC Main] | Adds locking to each pair.                                           |          |               |

### System Info

| Range     | DCF Integration     | Cassandra Compliant     | Linked Components     | Exported Components     |
|-----------|---------------------|-------------------------|-----------------------|-------------------------|
| 1.0.0.x   | No                  | Yes                     | -                     | -                       |
| 1.0.1.x   | No                  | Yes                     | -                     | -                       |
| 1.1.1.x   | No                  | Yes                     | -                     | -                       |
| 1.1.0.x   | No                  | Yes                     | -                     | -                       |
| 1.2.0.x   | No                  | Yes                     | -                     | -                       |

## Configuration

### Connections

#### Serial main connection

This connector uses a serial connection and requires the following input during element creation:

SERIAL CONNECTION:

- **IP address/host**: The polling IP of the device, e.g. *172.32.65.38*.
- **IP port**: The IP port of the device, e.g. *4001*.
- **Bus address**: Range 64 to 255.

## How to use

### General Page (Main View - v1.1.1.x)

This page displays general information, such as the **Model Number**, **Firmware Versions**, and **Control, Operating and Configuration Mode**

In all connector ranges **except v1.1.1x**, a page button allows you to set up the communication settings and amplifier addresses:

- **Port Baudrate, Parity, Stop Bits, Data Bits**

- **Amplifier 1 (A) Address, Amplifier 2 (B) Address, Amplifier 3 (C) Address**
  Note that these addresses must be filled in to enable the controller to poll generic individual HPA settings (see "HPA 1-3 Alarms Pages").

  The amplifier addresses range from 64 to 255 where 64 = @, 65 = A, 66 = B, etc.
  Each character is referred to by the DEC value. For more information, refer to <http://www.asciitable.com/>.

In range **v1.1.1.x**, the page also contains the **HPA-A Status**, **HPA-B Status**, **Waveguide Switch Status**, **PSU 1 Status**, **PSU 2 Status** and **Reset Faults button**.

### Control Page (not in v1.1.1.x)

This page displays control parameters for up to 4 switches, 2 attenuators and the RF for up to 3 HPAs connected to the controller.

### Status Page (not in v1.1.1.x)

This page displays the general **Status** of all 3 HPAs, the current **Waveguide Switch Status** and **PSU 1 and 2 Status**.

### HPA 1 -3 Alarms Pages (not in v1.1.1.x)

These are 3 pages that each represent the main faults and alarms for their respective HPA.

Polling for these 3 pages is disabled by default. Polling will only occur if you toggle the **Poll HPA X Alarms** parameter to *Enabled* AND you have provided the amplifier addresses (see "General Page").

If you need more detailed status information or settings for the individual HPAs, use the **XTU-400K** connector for individual HPA elements.

### Display (only in v1.1.1.x)

This page displays the **Screen Display** and its respective **Screen Lines**.

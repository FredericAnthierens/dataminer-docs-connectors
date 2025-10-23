---
uid: Connector_help_Fujitsu_FLEXR
---

# Fujitsu FLEXR

## About

The Fujitsu FLEXR is a management system used to maintain and monitor a wide variety of Fujitsu network elements.

## Configuration

### Connections

#### SNMP Primary Connection

This connector uses a Simple Network Management Protocol (SNMP) connection and requires the following input during element creation:

SNMP CONNECTION:

- **IP address/host**: The polling IP of the device.

SNMP Settings:

- **IP port**: The IP port of the device, by default *161*.
- **Get community string**: The community string used when reading values from the device, by default *public*.
- **Set community string**: The community string used when setting values on the device, by default *private.*

#### SNMP Secondary Connection

This connector uses a Simple Network Management Protocol (SNMP) connection and requires the following input during element creation:

SNMP CONNECTION:

- **IP address/host**: The polling IP of the device.

SNMP Settings:

- **IP port**: The IP port of the device, by default *161*.
- **Get community string**: The community string used when reading values from the device, by default *public*.
- **Set community string**: The community string used when setting values on the device, by default *private.*

### Initialization

For both the main and backup connections, the authentication information can be configured in the **Redundancy** table via the **User Name** and **Password** columns.

Either the primary or the main connection can be selected, and both connections can be enabled or disabled, after which the connector will automatically continue with the preferred connection.

### Redundancy

The connector has a main and backup connection available.

## How to use

### General

The **General** page contains everything related to the device connections. All communication can be enabled or disabled via **Enable Communication**

If the connector is communicating with the device, the **Connection Status** will be *Connected*, otherwise it is *Not Connected*. If communication has been disabled, this state is *Manually Disconnected*.

### Alarms

The **Alarm** page contains a table showing all the received alarms.

### Auto Events

The **Auto Events** page has a table containing captured auto events (unsolicited TL1 message).

### Auto Alarms

The **Auto Alarms** page has a table containing captured auto alarms (unsolicited TL1 message). Since auto alarms cannot be polled, rows here can be removed manually/automatically to avoid sticky alarms.

To remove alarms manually:

1. Select the rows that you want to delete.
1. Right-click the **Auto Alarms** table to open up a context menu.
1. Select the **Remove Alarm(s)** option to remove the rows.

To have alarms removed automatically:

1. Enable the **Auto Clear Old Auto Alarms** toggle button.
1. Set the **Max Age of Auto Alarms** to determine the criteria for automatic alarm removal.

### Inventory

The **Inventory** page shows all network elements in the inventory. This inventory has to be provisioned via a CSV file.

The Inventory table will generate DVE elements for each entry in the inventory CSV. Each DVE shows only the alarms corresponding with the relevant ID (based on the Source ID parameter in the Alarms table).

CSV example:

```txt
id;type
DeviceId1;Type1
DeviceId2;Type2
```


---
uid: Connector_help_Ciena_Blue_Planet_MCP_NMS
---

# Ciena Blue Planet MCP NMS

## About

Ciena's Blue Planet Manage, Control and Plan (MCP) domain controller brings software-defined programmability to Ciena network and service operations. It eliminates manual steps between separate management tools.

This HTTP connector is used to monitor and configure the Ciena Blue Planet domain controller.

## Configuration

### Connections

#### HTTP Main Connection

This connector uses an HTTP connection and requires the following input during element creation:

HTTP CONNECTION:

- **IP address/host**: The polling IP or URL of the destination.
- **IP port**: The IP port of the destination (default: *443*).
- **Device address**: The bus address of the device. If the proxy server has to be bypassed, specify *BypassProxy*.

### Initialization

For the connector to work properly, you need to specify the username and password on the General page.

### Web Interface

The web interface is only accessible when the client machine has network access to the product.

## How to use

The element consists of the following data pages:

- **General**: Allows you to specify the username and password to log in. A status parameter indicates whether you are logged in or logged out.
- **Network Elements**: Contains the Network Elements table.
- **Equipment**: Contains a table with the existing equipment per network element.
- **Active Alarms**: Lists the active alarms. A subpage summarizes the number of active alarms per category (Warning, Minor, Major, Critical, and Total). Enable the **Active Alarms Retrieve Affected Services** parameter to get data about the affected services in the Active Alarms table. For each new service-affecting alarm, an extra API call is used to retrieve the data of the affected services.
- **Alarms History**: Contains the Alarms History table. On a subpage, you can set the alarms history range.

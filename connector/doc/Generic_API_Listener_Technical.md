---
uid: Connector_help_Generic_API_Listener_Technical
---

# Generic API Listener

## About

This connector provides the ability for users to listen for incoming API requests called from a user-defined address. The received requests are processed and stored in table with all the relevant meaningful data.

You can forward the received request data for further processing, for example by a script defined in the DataMiner System.

## Configuration

### Connections

### Virtual Connection - Main

This connector uses a virtual connection and does not require any input during element creation.

### General

The General page displays a general **Status** parameter of the listener, which indicates whether the listener is currently active or not.

Underneath the **Status** parameter, listener **API Configuration** parameters are displayed.

The following parameters can be configured:

- **API Mode**: Allows you to set the mode of the API listener to *HTTP* or *HTTPS* to make the listener listen for HTTP or HTTPS requests, respectively. Note that for HTTPS requests to function correctly, you will need to select the necessary certificate on the **Configuration** subpage.
- **API Address**: The address where the listener will listen for incoming requests. This is a read-only parameter that is based on the other configuration parameters.
- **API IP/Hostname**: The IP address or hostname where the listener will listen for incoming requests.
- **API Path**: The path where the listener will listen for incoming requests.
- **API Port**: The port where the listener will listen for incoming requests.

In the lower-right corner of the page, the **Configuration** page button opens a subpage with additional configuration parameters.

### Configuration

This page contains extra configuration supported by the API listener.

#### HTTPS Certificates Configuration

At the top of the page, you can select the **HTTPS Certificate** to be used for HTTPS requests. You can select any of the certificates available on the DataMiner System; however, these certificates need to be **manually added to the system** first.

Below the dropdown where you can select the certificate, a refresh button is available to update the selection list.

#### Script Configuration

You can select a **script** that will be executed when the **execution interval** has elapsed. The script can be used to process the request data or perform any other custom logic. You can select any of the available scripts on the DataMiner System, as well as manually refresh the list by clicking the **Refresh** button.

As part of the script configuration, you can also define the **Script Parameter Unprocessed Keys** parameter. This determines which parameter in the script will accept the unprocessed keys from the request data table. The keys are passed to the script as a comma-separated list. This parameter can be disabled as well.

Finally, you can define the **Execution Interval** for the selected script. This parameter determines how often the script will be executed.

#### Access Tokens

Lastly, you can define the **Access Tokens** that are used to authenticate the incoming requests. You can add, edit, or delete access tokens from the table of available access tokens.

The access token table contains the following columns:

- **Name**: The name of the access token.
- **Token**: The value of the access token.
- **Expiry Date**: The expiry date of the access token.

### Requests Data

This page contains a table with an overview of all received requests.

The table contains the following columns:

- **Received ID**: The unique identifier of the received request.
- **URL**: The URL of the received request.
- **HTTP Address**: The HTTP address of the received request.
- **HTTP Action**: The HTTP action of the received request.
- **HTTP Headers**: The HTTP headers of the received request.
- **HTTP Body**: The HTTP body of the received request.
- **Received Time**: The time when the request was received.
- **Status**: The status of the received request.
- **Action**: Button to delete a row from the table.

In the top-right corner, the **Clear Table** button can be used to clear data from the table.

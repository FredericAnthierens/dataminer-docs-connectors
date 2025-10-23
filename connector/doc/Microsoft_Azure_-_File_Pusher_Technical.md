---
uid: Connector_help_Microsoft_Azure_-_File_Pusher_Technical
---

# Microsoft Azure - File Pusher

The Azure File Pusher connector is used to automate file synchronization from local storage to Azure Blob Storage.

Azure File Pusher acts as an enhanced Azure Storage Upload wrapper, providing an easy and intuitive way to configure links between local storage and Azure Storage. It allows periodic uploads of local files to Azure Storage, where their content can be used for further analysis or online access.

Credentials for authentication are securely stored withing the collector and used every time files are uploaded. Credentials can also be tested within the connector to make sure a valid token for file uploads is received when authenticating.

You can configure multiple file path combinations, each with dedicated upload settings, allowing flexible file transfers to the Azure Storage that best fits your use case. File paths are added, edited or deleted through the right-click context menu in the File Paths table.

## Configuration

### Connections

#### HTTP Main Connection

This connector uses an HTTP connection. However, this requires no input from the user during element creation.

### Initialization

When the element has been created, on the **General** page, configure and test the Azure Storage credentials (Tenant ID, Client ID, and Client Secret) and the Storage URL before you proceed with setting up file path combinations.

## How to use

### General Page

On the **General** page, the authentication parameters and storage URL should be configured:

- **Tenant ID**: A unique identifier associated with an Azure Active Directory (Azure AD) instance that represents a specific organization or tenant in Azure's directory structure. It can be found in the Overview section of Azure Active Directory under the Tenant Information.
- **Client ID**: A unique identifier, also known as Application ID, assigned to an application registered in Azure Active Directory (Azure AD). It is linked to the application registered in Azure and can be found in the application overview.
- **Client Secret**: A password-like credential used by applications registered in Azure Active Directory (Azure AD) to securely authenticate.
- **Blob Storage URL**: The endpoint used to access resources within an Azure Storage account (e.g. `https://dataminer.blob.core.windows.net`).

The **Test Authentication** button can be used to test whether the provided credentials can retrieve the valid token used to access the blob storage. The **Authentication Test** parameter will indicate whether the authentication test was successful (*OK*) or unsuccessful (*Error*).

### Configuration Page

To ensure that file uploads do not get stuck indefinitely, a safety measure has been implemented. On the Configuration page, you can set parameters that will automatically terminate an upload if certain conditions are met.

Specifically, you can configure the system to terminate uploads after a specified number of **failures** or after a certain **duration (in minutes)**.

This helps maintain the efficiency and reliability of the upload process by preventing prolonged or failed uploads from consuming resources unnecessarily.

### File Paths Page

On the **File Paths** page, you can find a table containing source-destination information and settings for file uploads. Table rows can be added, edited, or deleted through the right-click menu.

- **Source Path**: The local absolute source path, from which the files are uploaded.
- **Container**: The Azure container name, relative to storage mentioned in the Storage URL parameter, to which files are uploaded.
- **Custom Path Prefix**: The prefix path, added to the original file path, when the file is uploaded to Azure.
- **Timer**: Timer defining the frequency with which rows of the File Paths table are uploaded to Azure.
- **Recursive**: Defines if files in the source path are searched recursively in all directories or only in the top directory of the path.
- **Overwrite**: Determines whether files will be overwritten if these same files have already been uploaded.
- **Tries**: Specifies the number of attempts to retry uploading a file if the initial upload fails.
- **Auto Delete on Success**: Determines whether successfully pushed files are deleted from the source path.
- **Upload**: Triggers an upload of files from the selected local path to the container path.

The **Upload All** button will trigger an upload of all files from the File Paths table.

## Notes

For a better user experience, this connector can be used together with the [**Microsoft Azure Cloud Platform**](xref:Connector_help_Microsoft_Azure) connector, which allows you to monitor relevant resource metrics available in Azure.


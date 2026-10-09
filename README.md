# WIZ


This repository explains about how I POV’d and productioni-zed WIZ

First and foremost, wiz locks down their documentation behind their tenant. Their POC/POV tenant is set to expire in 21 days. If success criteria is not met in that timeframe, you can work with the sales team to get an extension with a new expiration date.

After the tenant is provisioned first thing to check would be what are you licensed for as they have 3 main products - Cloud (CSPM), Code (their scanner), Code Lite (bring your own scanner), Defend (runtime security). You can check for licensing under settings —> license to see what products is the tenant licensed for you to test.

Wiz Cloud (POV)

Azure Connector - you can connect using management group, subscription or you have a choice to explicitly also scan Entra ID only for CIEM (Cloud Identity Entitlement Management)

Pre-Requisites when creating a connection in Wiz
  1. Azure Tenant ID
  2. Management Group ID / Subscription ID

I chose to connect to one subscription which has many resources to give me a good idea on what the scan found which helps me compare to Google SCCE and Defender.

The integration was fairly straight forward, an instance of Wiz app registration in the form of a service principal (enterprise app) is provisioned in Entra ID by Wiz.

You also create 3 Custom IAM roles 
  1. WizCustomRole - Permissions on Compute, Registry, Vaults, Storage.
  2. WizDataScanningRole - Permissions on SQL Databases
  3. WizServerlessScanningRole - Permissions on backups and functions.




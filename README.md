# WIZ


This repository explains about how I POV’d and productioni-zed WIZ

First and foremost, wiz locks down their documentation behind their tenant. Their POC/POV tenant is set to expire in 21 days. If success criteria is not met in that timeframe, you can work with the sales team to get an extension with a new expiration date.

After the tenant is provisioned first thing to check would be what are you licensed for as they have 3 main products - Cloud (CSPM), Code (their scanner), Code Lite (bring your own scanner), Defend (runtime security). You can check for licensing under settings —> license to see what products is the tenant licensed for you to test.

Wiz Cloud (POV)

Azure - I chose to connect to one subscription. The integration was fairly straight forward, when it comes to creating an app registration and an enterprise app. one pre-requisite is to make sure the Azure app id that gets provisioned during the integration in WIZ is used in the azure tenant.

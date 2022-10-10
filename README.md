# Integration-Examples
Examples include API calls, Middleware Content and Coding


## Postman Collection

### Importing Environmant and Collection into postman
Download the collection and the environment from folder [SAP SuccessFactors HXM Suite API Examples](https://github.com/d040159/Integration-Examples/tree/main/SAP%20SuccessFactors%20HXM%20Suite%20API%20Examples). Go to postman and use the File-->Import menu to select those two files from your Download-Folder and import them. 

### Prepare the environment by adding your system specific data and credential
Open the environment in postman to edit the environment variables.
|Variable        | Content                   | Example    |
|----------------|---------------------------|------------|
|APIUserName     | Username of the API user  | sfadmin    |
|APIUserPassword | Password if API user      | Secret123! |
|OAuthClientID   | API key or Client ID from oAuth2 client registration in SuccessFactors | ODgwMzU4YmQ2Yjg1Zm12MWE4OWNjOWExOWRhZf |
|OAuthPrivateKey | Private key from oAuth2 client registration in SuccessFactors | TUlJRER.....zN4UFh2NyMjI2ZhbHNl |

The Endpoints URL in this collections are predefined for Salesdemo environment in DC4 which is apisalesdemo4.successfactors.com. In case you use a different DC ensure to put the right URLs here as listed in our documentation on [help.sap.com](https://help.sap.com/docs/SAP_SUCCESSFACTORS_PLATFORM/d599f15995d348a1b45ba5603e2aba9b/af2b8d5437494b12be88fe374eba75b6.html)
- 
3. To use the collection execture first the "Generate SAML assertion" API requets in the main folder
4. Execute the "Request oAuth 

# Integration-Examples
Examples include API calls, Middleware Content and Coding


## Postman Collection

### Importing Environmant and Collection into postman
Download the collection and the environment from folder [SAP SuccessFactors HXM Suite API Examples](https://github.com/d040159/Integration-Examples/tree/main/SAP%20SuccessFactors%20HXM%20Suite%20API%20Examples). Go to postman and use the File-->Import menu to select those two files from your Download-Folder and import them. 

### Prepare the environment by adding your system specific data and credential
Open the environment in postman to edit the environment variables.
|Variable        | Content                   | Example    |
|----------------|---------------------------|------------|
|APIUserName     | Username of the API user  | sfapi      |
|APIUserPassword | Password if API user      | Secret123! |
|OAuthClientID   | API key or Client ID from oAuth2 client registration in SuccessFactors | ODgwMzU4YmQ2Yjg1Zm12MWE4OWNjOWExOWRhZf |
|OAuthPrivateKey | Private key from oAuth2 client registration in SuccessFactors | TUlJRER.....zN4UFh2NyMjI2ZhbHNl |


The Endpoints URL in this collections are predefined for Salesdemo environment in DC4 which is apisalesdemo4.successfactors.com. In case you use a different DC ensure to put the right URLs here as listed in our documentation on [help.sap.com](https://help.sap.com/docs/SAP_SUCCESSFACTORS_PLATFORM/d599f15995d348a1b45ba5603e2aba9b/af2b8d5437494b12be88fe374eba75b6.html)

### Using the postman collection
1.  Use the recenly configure environment variable and select it in the postman environment drop down in the uper right corner of postman
2.  Open the collection and send the request for *generate SAML assertion*. Note that this call is a simplification for handling this postman collection and should not be used as such in any productive environments this call should also not be done/used in any coding. The right approach to generate a SAML assertion for a technical user is explained here: https://blogs.sap.com/2021/09/06/best-practice-for-saml-offline-generator-and-local-keystore-with-sap-successfactors/    
3.  After generating the SAML assertion for your API User use the *request access token* API call to get the access token to do the final API calls.
4. Open any folder and call the API using the access token

Note: SAML assertions and access tokens expire after 10 minutes or 24hours.

### Understanding the API examples in the collections
API examples in this collection are structured by the SAP SuccessFactors modules and their entities. For example *SAP SuccessFactors Employee Central* is the moduel providing core HR data and hence you will fine there in corresponding Sub-Folders entities such as *PerPerson* for Biographical Information or *EmpJob* for the Job related historic information of an Employee.

Some of the examples are build in a way that the order of the execution of API calls matters, e.g. the Folder "Compound Employee SOAP API" demonstrates the usage of oAuth2 with the SOAP API and changes first some data, before it does the SOAP login to create a session, followed by several SOAP Querries. 

The examples in the *SAP SuccessFactors Platform* Folder are also documented in this blog: https://blogs.sap.com/2022/08/18/demystify-sap-successfactors-role-based-permission-apis/ 

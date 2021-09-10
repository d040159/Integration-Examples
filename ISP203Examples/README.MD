# Overview
In this folder you can find the postman collection and environment and well as the SAP SuccessFactors integration flow which demonstrates the consumption of SAP SuccessFactors SOAP and OData APIs using oAuth2 with SAML Bearer Assertion or Basic Authentication.

The following scenarios are supported in Postman in the provided collection and environment:
* Calling SAP SuccessFactors OData APIs using oAuth2 with SAML Bearer Assertion 
* Calling SAP SuccessFactors OData APIs using Basic Authentication 
* Calling SAP SuccessFactors SOAP APIs using oAuth2 with SAML Bearer Assertion
* Calling SAP SuccessFactors SOAP APIs using Basic Authentication 
* Triggering a sender based SAP Cloud Integration Flow using X-CSRF Token

The following secenarios are supported by the provided integration flow in SAP Cloud Integration Suite: 
* Calling SAP SuccessFactors SOAP and OData APIs using oAuth2 with SAML Bearer Assertion

# Postman collection and Environment

## Step 1
Download and install Postman v8.10.0 or later

## Step 2
Download the environment file and the collection file to your computer

## Step 3
Import the environment file and the collection into your postman

## Step 4
Provide values for all variable in the environment which are marked with entries in brackets like this one: <your SAP SuccessFactors API username>
![Environment Hints](./Images/EnvironmentHints.jpg)
# SAP Cloud Integration Flow

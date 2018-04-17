# Ballerina SCIM Endpoint

*The system for Cross-domain Identity Management (SCIM) specification
 is designed to make managing user identities in cloud-based applications 
 and services easier.*

 
 The Ballerina SCIM2 Endpoint allows users to access Rest API of any service that implements 
 SCIM2 specification.  
 
 
 ## Compatibility
 | Language Version        | Endpoint Version          | API Versions  |
 | ------------- |:-------------:| -----:|
 | ballerina-0.970.0-beta1-SNAPSHOT     | 0.9.3 | SCIM2.0 |
 
![alt text](resources/SCIM2.png)

## Working with SCIM Endpoint actions

In order for you to use the SCIM Endpoint, first you need to create a SCIM2 Client 
endpoint.

```ballerina
import wso2/scim2;

endpoint scim2:Client scimEP {
    baseUrl:"https://localhost:9443",
    clientConfig:{
                     auth:{
                              scheme:"oauth",
                              accessToken:"<......>",
                              clientId:"<......>",
                              clientSecret:"<......>",
                              refreshToken:"<......>",
                              refreshUrl:"<......>"
                          },
                     targets:[{url:"https://localhost:9443",
                                  secureSocket:{
                                                   trustStore:{
                                                                  filePath:"<......>",
                                                                  password:"<......>"
                                                              }
                                               }
                              }]
                 }
};
```
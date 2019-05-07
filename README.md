# ![LOGO](logo.png) ApiManagementClient **flow**ground Connector

## Description

A generated **flow**ground connector for the ApiManagementClient API (version 2016-10-10).

Generated from: https://api.apis.guru/v2/specs/azure.com/apimanagement-apimcertificates/2016-10-10/swagger.json<br/>
Generated at: 2019-05-07T17:37:08+03:00

## API Description

Use these REST APIs for performing operations on Certificate entity in your Azure API Management deployment. Certificates can be used to setup mutual authentication with your Backend in API Management. For more information refer to [How to secure backend using Mutual Auth Certificate](https://docs.microsoft.com/en-us/azure/api-management/api-management-howto-mutual-certificates).

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists a collection of all certificates in the specified service instance.

*Tags:* `Certificates`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `$filter` - _optional_ - | Field          | Supported operators    | Supported functions                         |
|----------------|------------------------|---------------------------------------------|
| id             | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| subject        | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| thumbprint     | ge, le, eq, ne, gt, lt | substringof, contains, startswith, endswith |
| expirationDate | ge, le, eq, ne, gt, lt | N/A                                         |
* `$top` - _optional_ - Number of records to return.
* `$skip` - _optional_ - Number of records to skip.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Deletes specific certificate.

*Tags:* `Certificates`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `certificateId` - _required_ - Identifier of the certificate entity. Must be unique in the current API Management service instance.
* `If-Match` - _required_ - The entity state (Etag) version of the certificate to delete. A value of "*" can be used for If-Match to unconditionally apply the operation.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Gets the details of the certificate specified by its identifier.

*Tags:* `Certificates`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `certificateId` - _required_ - Identifier of the certificate entity. Must be unique in the current API Management service instance.
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

### Creates or updates the certificate being used for authentication with the backend.

*Tags:* `Certificates`

#### Input Parameters
* `resourceGroupName` - _required_ - The name of the resource group.
* `serviceName` - _required_ - The name of the API Management service.
* `certificateId` - _required_ - Identifier of the certificate entity. Must be unique in the current API Management service instance.
* `If-Match` - _optional_ - The entity state (Etag) version of the certificate to update. A value of "*" can be used for If-Match to unconditionally apply the operation..
* `api-version` - _required_ - Version of the API to be used with the client request.
* `subscriptionId` - _required_ - Subscription credentials which uniquely identify Microsoft Azure subscription. The subscription ID forms part of the URI for every service call.

## License

**flow**ground :- Telekom iPaaS / azure-com-apimanagement-apimcertificates-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.

# SomeonesComputerSdk

JSON-LD resources backing the control panel. Bearer-token reachable since #1418 — see docs/sdk-generation.md.


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/SomeonesComputerSdk/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure Bearer authorization: bearerAuth
$config = SomeonesComputer\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new SomeonesComputer\Sdk\Api\AdoptionApprovalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int | The collection page number

try {
    $result = $apiInstance->apiAdoptionApprovalsGetCollection($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdoptionApprovalApi->apiAdoptionApprovalsGetCollection: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AdoptionApprovalApi* | [**apiAdoptionApprovalsGetCollection**](docs/Api/AdoptionApprovalApi.md#apiadoptionapprovalsgetcollection) | **GET** /api/adoption_approvals | Retrieves the collection of AdoptionApproval resources.
*AdoptionApprovalApi* | [**apiAdoptionApprovalsIdDelete**](docs/Api/AdoptionApprovalApi.md#apiadoptionapprovalsiddelete) | **DELETE** /api/adoption_approvals/{id} | Removes the AdoptionApproval resource.
*AdoptionApprovalApi* | [**apiAdoptionApprovalsIdGet**](docs/Api/AdoptionApprovalApi.md#apiadoptionapprovalsidget) | **GET** /api/adoption_approvals/{id} | Retrieves a AdoptionApproval resource.
*AdoptionApprovalApi* | [**apiAdoptionApprovalsPost**](docs/Api/AdoptionApprovalApi.md#apiadoptionapprovalspost) | **POST** /api/adoption_approvals | Creates a AdoptionApproval resource.
*ApplicationApi* | [**apiApplicationsGetCollection**](docs/Api/ApplicationApi.md#apiapplicationsgetcollection) | **GET** /api/applications | Retrieves the collection of Application resources.
*ApplicationApi* | [**apiApplicationsIdDelete**](docs/Api/ApplicationApi.md#apiapplicationsiddelete) | **DELETE** /api/applications/{id} | Removes the Application resource.
*ApplicationApi* | [**apiApplicationsIdGet**](docs/Api/ApplicationApi.md#apiapplicationsidget) | **GET** /api/applications/{id} | Retrieves a Application resource.
*ApplicationApi* | [**apiApplicationsIdPatch**](docs/Api/ApplicationApi.md#apiapplicationsidpatch) | **PATCH** /api/applications/{id} | Updates the Application resource.
*ApplicationApi* | [**apiApplicationsPost**](docs/Api/ApplicationApi.md#apiapplicationspost) | **POST** /api/applications | Creates a Application resource.
*CreditTransactionApi* | [**apiCreditTransactionsGetCollection**](docs/Api/CreditTransactionApi.md#apicredittransactionsgetcollection) | **GET** /api/credit_transactions | Retrieves the collection of CreditTransaction resources.
*CreditTransactionApi* | [**apiCreditTransactionsIdGet**](docs/Api/CreditTransactionApi.md#apicredittransactionsidget) | **GET** /api/credit_transactions/{id} | Retrieves a CreditTransaction resource.
*DeploymentApi* | [**apiDeploymentsGetCollection**](docs/Api/DeploymentApi.md#apideploymentsgetcollection) | **GET** /api/deployments | Retrieves the collection of Deployment resources.
*DeploymentApi* | [**apiDeploymentsIdDelete**](docs/Api/DeploymentApi.md#apideploymentsiddelete) | **DELETE** /api/deployments/{id} | Removes the Deployment resource.
*DeploymentApi* | [**apiDeploymentsIdGet**](docs/Api/DeploymentApi.md#apideploymentsidget) | **GET** /api/deployments/{id} | Retrieves a Deployment resource.
*DeploymentApi* | [**apiDeploymentsIdPatch**](docs/Api/DeploymentApi.md#apideploymentsidpatch) | **PATCH** /api/deployments/{id} | Updates the Deployment resource.
*DeploymentApi* | [**apiDeploymentsIdendpointsGetCollection**](docs/Api/DeploymentApi.md#apideploymentsidendpointsgetcollection) | **GET** /api/deployments/{id}/endpoints | Retrieves the collection of Deployment resources.
*DeploymentApi* | [**apiDeploymentsPost**](docs/Api/DeploymentApi.md#apideploymentspost) | **POST** /api/deployments | Creates a Deployment resource.
*DeploymentApi* | [**bundleUploadConfirm**](docs/Api/DeploymentApi.md#bundleuploadconfirm) | **POST** /api/deployments/bundle_uploads/confirm | Creates a Deployment resource.
*DeploymentApi* | [**bundleUploadDeclare**](docs/Api/DeploymentApi.md#bundleuploaddeclare) | **POST** /api/deployments/bundle_uploads | Creates a Deployment resource.
*ManagedServiceApi* | [**apiManagedServicesGetCollection**](docs/Api/ManagedServiceApi.md#apimanagedservicesgetcollection) | **GET** /api/managed_services | Retrieves the collection of ManagedService resources.
*ManagedServiceApi* | [**apiManagedServicesIdDelete**](docs/Api/ManagedServiceApi.md#apimanagedservicesiddelete) | **DELETE** /api/managed_services/{id} | Removes the ManagedService resource.
*ManagedServiceApi* | [**apiManagedServicesIdGet**](docs/Api/ManagedServiceApi.md#apimanagedservicesidget) | **GET** /api/managed_services/{id} | Retrieves a ManagedService resource.
*ManagedServiceApi* | [**apiManagedServicesPost**](docs/Api/ManagedServiceApi.md#apimanagedservicespost) | **POST** /api/managed_services | Creates a ManagedService resource.
*ManagedServiceApi* | [**resume**](docs/Api/ManagedServiceApi.md#resume) | **POST** /api/managed_services/{id}/resume | Creates a ManagedService resource.
*ManagedServiceApi* | [**suspend**](docs/Api/ManagedServiceApi.md#suspend) | **POST** /api/managed_services/{id}/suspend | Creates a ManagedService resource.
*OrganizationApi* | [**apiOrganizationsGetCollection**](docs/Api/OrganizationApi.md#apiorganizationsgetcollection) | **GET** /api/organizations | Retrieves the collection of Organization resources.
*OrganizationApi* | [**apiOrganizationsIdDelete**](docs/Api/OrganizationApi.md#apiorganizationsiddelete) | **DELETE** /api/organizations/{id} | Removes the Organization resource.
*OrganizationApi* | [**apiOrganizationsIdGet**](docs/Api/OrganizationApi.md#apiorganizationsidget) | **GET** /api/organizations/{id} | Retrieves a Organization resource.
*OrganizationApi* | [**apiOrganizationsIdPatch**](docs/Api/OrganizationApi.md#apiorganizationsidpatch) | **PATCH** /api/organizations/{id} | Updates the Organization resource.
*OrganizationApi* | [**apiOrganizationsPost**](docs/Api/OrganizationApi.md#apiorganizationspost) | **POST** /api/organizations | Creates a Organization resource.
*ServiceBindingApi* | [**apiServiceBindingsGetCollection**](docs/Api/ServiceBindingApi.md#apiservicebindingsgetcollection) | **GET** /api/service_bindings | Retrieves the collection of ServiceBinding resources.
*ServiceBindingApi* | [**apiServiceBindingsIdDelete**](docs/Api/ServiceBindingApi.md#apiservicebindingsiddelete) | **DELETE** /api/service_bindings/{id} | Removes the ServiceBinding resource.
*ServiceBindingApi* | [**apiServiceBindingsIdGet**](docs/Api/ServiceBindingApi.md#apiservicebindingsidget) | **GET** /api/service_bindings/{id} | Retrieves a ServiceBinding resource.
*ServiceBindingApi* | [**apiServiceBindingsPost**](docs/Api/ServiceBindingApi.md#apiservicebindingspost) | **POST** /api/service_bindings | Creates a ServiceBinding resource.
*SwarmApi* | [**apiSwarmsGetCollection**](docs/Api/SwarmApi.md#apiswarmsgetcollection) | **GET** /api/swarms | Retrieves the collection of Swarm resources.
*SwarmApi* | [**apiSwarmsIdDelete**](docs/Api/SwarmApi.md#apiswarmsiddelete) | **DELETE** /api/swarms/{id} | Removes the Swarm resource.
*SwarmApi* | [**apiSwarmsIdGet**](docs/Api/SwarmApi.md#apiswarmsidget) | **GET** /api/swarms/{id} | Retrieves a Swarm resource.
*SwarmApi* | [**apiSwarmsIdPatch**](docs/Api/SwarmApi.md#apiswarmsidpatch) | **PATCH** /api/swarms/{id} | Updates the Swarm resource.
*SwarmApi* | [**apiSwarmsPost**](docs/Api/SwarmApi.md#apiswarmspost) | **POST** /api/swarms | Creates a Swarm resource.

## Models

- [AdoptionApproval](docs/Model/AdoptionApproval.md)
- [AdoptionApprovalAdoptionApprovalInput](docs/Model/AdoptionApprovalAdoptionApprovalInput.md)
- [Application](docs/Model/Application.md)
- [ApplicationJsonMergePatch](docs/Model/ApplicationJsonMergePatch.md)
- [BundleAdditionalContextInput](docs/Model/BundleAdditionalContextInput.md)
- [BundleContextInput](docs/Model/BundleContextInput.md)
- [BundleForwardedImageInput](docs/Model/BundleForwardedImageInput.md)
- [BundleUploadTarget](docs/Model/BundleUploadTarget.md)
- [ConstraintViolation](docs/Model/ConstraintViolation.md)
- [ConstraintViolationViolationsInner](docs/Model/ConstraintViolationViolationsInner.md)
- [CreditTransaction](docs/Model/CreditTransaction.md)
- [CreditTransactionEngineMillis](docs/Model/CreditTransactionEngineMillis.md)
- [CreditTransactionUsageBytes](docs/Model/CreditTransactionUsageBytes.md)
- [Deployment](docs/Model/Deployment.md)
- [DeploymentBundleUploadConfirmInput](docs/Model/DeploymentBundleUploadConfirmInput.md)
- [DeploymentBundleUploadConfirmOutput](docs/Model/DeploymentBundleUploadConfirmOutput.md)
- [DeploymentBundleUploadDeclareInput](docs/Model/DeploymentBundleUploadDeclareInput.md)
- [DeploymentBundleUploadDeclareOutput](docs/Model/DeploymentBundleUploadDeclareOutput.md)
- [DeploymentDeploymentEndpoint](docs/Model/DeploymentDeploymentEndpoint.md)
- [DeploymentJsonMergePatch](docs/Model/DeploymentJsonMergePatch.md)
- [DeploymentJsonMergePatchBuildContextsValueValue](docs/Model/DeploymentJsonMergePatchBuildContextsValueValue.md)
- [DeploymentJsonMergePatchCanonicalSpecValue](docs/Model/DeploymentJsonMergePatchCanonicalSpecValue.md)
- [DeploymentVariable](docs/Model/DeploymentVariable.md)
- [Error](docs/Model/Error.md)
- [Failure](docs/Model/Failure.md)
- [Machine](docs/Model/Machine.md)
- [ManagedService](docs/Model/ManagedService.md)
- [ManagedServiceLastLoadMillis](docs/Model/ManagedServiceLastLoadMillis.md)
- [ManagedServiceManagedServiceInput](docs/Model/ManagedServiceManagedServiceInput.md)
- [ManagedServicePendingLoadMillis](docs/Model/ManagedServicePendingLoadMillis.md)
- [ManagedServiceQuotaBytes](docs/Model/ManagedServiceQuotaBytes.md)
- [ManagedServiceUsageBytes](docs/Model/ManagedServiceUsageBytes.md)
- [Membership](docs/Model/Membership.md)
- [OAuthIdentity](docs/Model/OAuthIdentity.md)
- [Organization](docs/Model/Organization.md)
- [OrganizationJsonMergePatch](docs/Model/OrganizationJsonMergePatch.md)
- [OrganizationSignal](docs/Model/OrganizationSignal.md)
- [PortAllocation](docs/Model/PortAllocation.md)
- [ProxmoxInstance](docs/Model/ProxmoxInstance.md)
- [RecoveryCode](docs/Model/RecoveryCode.md)
- [SealedSecret](docs/Model/SealedSecret.md)
- [Service](docs/Model/Service.md)
- [ServiceBinding](docs/Model/ServiceBinding.md)
- [ServiceBindingServiceBindingInput](docs/Model/ServiceBindingServiceBindingInput.md)
- [ServiceCpuLimit](docs/Model/ServiceCpuLimit.md)
- [ServiceCpuReservation](docs/Model/ServiceCpuReservation.md)
- [ServiceHealthcheckValue](docs/Model/ServiceHealthcheckValue.md)
- [ServiceInstance](docs/Model/ServiceInstance.md)
- [ServiceInstanceCapacityBytes](docs/Model/ServiceInstanceCapacityBytes.md)
- [ServiceInstanceObservedUsageBytes](docs/Model/ServiceInstanceObservedUsageBytes.md)
- [ServiceMemLimit](docs/Model/ServiceMemLimit.md)
- [ServiceMemReservation](docs/Model/ServiceMemReservation.md)
- [ServicePortsInnerValue](docs/Model/ServicePortsInnerValue.md)
- [Swarm](docs/Model/Swarm.md)
- [SwarmJsonMergePatch](docs/Model/SwarmJsonMergePatch.md)
- [SwarmNode](docs/Model/SwarmNode.md)
- [User](docs/Model/User.md)
- [UserAvatarPhoto](docs/Model/UserAvatarPhoto.md)
- [Variable](docs/Model/Variable.md)
- [VariableVersion](docs/Model/VariableVersion.md)

## Authorization

Authentication schemes defined for the API:
### bearerAuth

- **Type**: Bearer authentication

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
    - Generator version: `7.11.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`

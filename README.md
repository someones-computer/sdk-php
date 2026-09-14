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
$adoption_approval_adoption_approval_input = new \SomeonesComputer\Sdk\Model\AdoptionApprovalAdoptionApprovalInput(); // \SomeonesComputer\Sdk\Model\AdoptionApprovalAdoptionApprovalInput | The new AdoptionApproval resource

try {
    $result = $apiInstance->adoptionApprovalsDecide($adoption_approval_adoption_approval_input);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AdoptionApprovalApi->adoptionApprovalsDecide: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AdoptionApprovalApi* | [**adoptionApprovalsDecide**](docs/Api/AdoptionApprovalApi.md#adoptionapprovalsdecide) | **POST** /api/adoption_approvals | Creates a AdoptionApproval resource.
*AdoptionApprovalApi* | [**adoptionApprovalsGet**](docs/Api/AdoptionApprovalApi.md#adoptionapprovalsget) | **GET** /api/adoption_approvals/{id} | Retrieves a AdoptionApproval resource.
*AdoptionApprovalApi* | [**adoptionApprovalsList**](docs/Api/AdoptionApprovalApi.md#adoptionapprovalslist) | **GET** /api/adoption_approvals | Retrieves the collection of AdoptionApproval resources.
*AdoptionApprovalApi* | [**adoptionApprovalsWithdraw**](docs/Api/AdoptionApprovalApi.md#adoptionapprovalswithdraw) | **DELETE** /api/adoption_approvals/{id} | Removes the AdoptionApproval resource.
*ApplicationApi* | [**applicationsCreate**](docs/Api/ApplicationApi.md#applicationscreate) | **POST** /api/applications | Creates a Application resource.
*ApplicationApi* | [**applicationsDelete**](docs/Api/ApplicationApi.md#applicationsdelete) | **DELETE** /api/applications/{id} | Removes the Application resource.
*ApplicationApi* | [**applicationsGet**](docs/Api/ApplicationApi.md#applicationsget) | **GET** /api/applications/{id} | Retrieves a Application resource.
*ApplicationApi* | [**applicationsList**](docs/Api/ApplicationApi.md#applicationslist) | **GET** /api/applications | Retrieves the collection of Application resources.
*ApplicationApi* | [**applicationsUpdate**](docs/Api/ApplicationApi.md#applicationsupdate) | **PATCH** /api/applications/{id} | Updates the Application resource.
*CreditTransactionApi* | [**creditTransactionsGet**](docs/Api/CreditTransactionApi.md#credittransactionsget) | **GET** /api/credit_transactions/{id} | Retrieves a CreditTransaction resource.
*CreditTransactionApi* | [**creditTransactionsList**](docs/Api/CreditTransactionApi.md#credittransactionslist) | **GET** /api/credit_transactions | Retrieves the collection of CreditTransaction resources.
*DeploymentApi* | [**deploymentsBundleUploadConfirm**](docs/Api/DeploymentApi.md#deploymentsbundleuploadconfirm) | **POST** /api/deployments/bundle_uploads/confirm | Creates a Deployment resource.
*DeploymentApi* | [**deploymentsBundleUploadDeclare**](docs/Api/DeploymentApi.md#deploymentsbundleuploaddeclare) | **POST** /api/deployments/bundle_uploads | Creates a Deployment resource.
*DeploymentApi* | [**deploymentsCreate**](docs/Api/DeploymentApi.md#deploymentscreate) | **POST** /api/deployments | Creates a Deployment resource.
*DeploymentApi* | [**deploymentsDelete**](docs/Api/DeploymentApi.md#deploymentsdelete) | **DELETE** /api/deployments/{id} | Removes the Deployment resource.
*DeploymentApi* | [**deploymentsEndpoints**](docs/Api/DeploymentApi.md#deploymentsendpoints) | **GET** /api/deployments/{id}/endpoints | Retrieves the collection of Deployment resources.
*DeploymentApi* | [**deploymentsGet**](docs/Api/DeploymentApi.md#deploymentsget) | **GET** /api/deployments/{id} | Retrieves a Deployment resource.
*DeploymentApi* | [**deploymentsList**](docs/Api/DeploymentApi.md#deploymentslist) | **GET** /api/deployments | Retrieves the collection of Deployment resources.
*DeploymentApi* | [**deploymentsUpdate**](docs/Api/DeploymentApi.md#deploymentsupdate) | **PATCH** /api/deployments/{id} | Updates the Deployment resource.
*ManagedServiceApi* | [**managedServicesCreate**](docs/Api/ManagedServiceApi.md#managedservicescreate) | **POST** /api/managed_services | Creates a ManagedService resource.
*ManagedServiceApi* | [**managedServicesDelete**](docs/Api/ManagedServiceApi.md#managedservicesdelete) | **DELETE** /api/managed_services/{id} | Removes the ManagedService resource.
*ManagedServiceApi* | [**managedServicesGet**](docs/Api/ManagedServiceApi.md#managedservicesget) | **GET** /api/managed_services/{id} | Retrieves a ManagedService resource.
*ManagedServiceApi* | [**managedServicesList**](docs/Api/ManagedServiceApi.md#managedserviceslist) | **GET** /api/managed_services | Retrieves the collection of ManagedService resources.
*ManagedServiceApi* | [**managedServicesResume**](docs/Api/ManagedServiceApi.md#managedservicesresume) | **POST** /api/managed_services/{id}/resume | Creates a ManagedService resource.
*ManagedServiceApi* | [**managedServicesSuspend**](docs/Api/ManagedServiceApi.md#managedservicessuspend) | **POST** /api/managed_services/{id}/suspend | Creates a ManagedService resource.
*OrganizationApi* | [**organizationsCreate**](docs/Api/OrganizationApi.md#organizationscreate) | **POST** /api/organizations | Creates a Organization resource.
*OrganizationApi* | [**organizationsDelete**](docs/Api/OrganizationApi.md#organizationsdelete) | **DELETE** /api/organizations/{id} | Removes the Organization resource.
*OrganizationApi* | [**organizationsGet**](docs/Api/OrganizationApi.md#organizationsget) | **GET** /api/organizations/{id} | Retrieves a Organization resource.
*OrganizationApi* | [**organizationsList**](docs/Api/OrganizationApi.md#organizationslist) | **GET** /api/organizations | Retrieves the collection of Organization resources.
*OrganizationApi* | [**organizationsUpdate**](docs/Api/OrganizationApi.md#organizationsupdate) | **PATCH** /api/organizations/{id} | Updates the Organization resource.
*ServiceBindingApi* | [**serviceBindingsCreate**](docs/Api/ServiceBindingApi.md#servicebindingscreate) | **POST** /api/service_bindings | Creates a ServiceBinding resource.
*ServiceBindingApi* | [**serviceBindingsDelete**](docs/Api/ServiceBindingApi.md#servicebindingsdelete) | **DELETE** /api/service_bindings/{id} | Removes the ServiceBinding resource.
*ServiceBindingApi* | [**serviceBindingsGet**](docs/Api/ServiceBindingApi.md#servicebindingsget) | **GET** /api/service_bindings/{id} | Retrieves a ServiceBinding resource.
*ServiceBindingApi* | [**serviceBindingsList**](docs/Api/ServiceBindingApi.md#servicebindingslist) | **GET** /api/service_bindings | Retrieves the collection of ServiceBinding resources.
*SwarmApi* | [**swarmsCreate**](docs/Api/SwarmApi.md#swarmscreate) | **POST** /api/swarms | Creates a Swarm resource.
*SwarmApi* | [**swarmsDelete**](docs/Api/SwarmApi.md#swarmsdelete) | **DELETE** /api/swarms/{id} | Removes the Swarm resource.
*SwarmApi* | [**swarmsGet**](docs/Api/SwarmApi.md#swarmsget) | **GET** /api/swarms/{id} | Retrieves a Swarm resource.
*SwarmApi* | [**swarmsList**](docs/Api/SwarmApi.md#swarmslist) | **GET** /api/swarms | Retrieves the collection of Swarm resources.
*SwarmApi* | [**swarmsUpdate**](docs/Api/SwarmApi.md#swarmsupdate) | **PATCH** /api/swarms/{id} | Updates the Swarm resource.

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

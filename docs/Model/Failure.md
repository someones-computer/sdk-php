# # Failure

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deployment** | **string** | Deleting a revision deletes its failures with it. They are an account of what that revision did, and outliving the thing they describe would leave a page that can only render half of itself. | [optional]
**proxmox_instance** | [**\SomeonesComputer\Sdk\Model\ProxmoxInstance**](ProxmoxInstance.md) |  | [optional]
**phase** | **string** |  | [optional]
**reason** | **string** | Verbatim, as it was written to &#x60;Deployment::$statusReason&#x60; at the time. | [optional]
**reference** | **string** | The short handle this failure is quoted by — see {@see FailureReference}. | [optional] [readonly]
**service** | **string** | Which compose service, where the phase happens per-service. Null for the phases that fail the revision as a whole (placement, stranded) and for a deploy that never got as far as naming one. | [optional]
**build_log_key** | **string** | Object key of the build log as it stood, or null when there was none. | [optional]
**image_digest** | **string** | The digest a {@see FailurePhase::Scan} failure was quarantined over — null for every other phase. What lets the scan quarantine queue (docs/image-scanning.md, #816) resolve straight from a quarantined revision to the exact {@see \\App\\Entity\\ImageScan} an operator&#39;s Clear or Uphold acts on, without re-deriving it from a pinned image reference or a reason string meant for a person to read. | [optional]
**share_token** | **string** | The capability that makes {@see \\App\\Controller\\FailureController::shared()} serve this to someone with no session, or null while it is private. | [optional] [readonly]
**shared_at** | **\DateTime** |  | [optional] [readonly]
**share_expires_at** | **\DateTime** | When the capability above stops working, 24 hours after it was minted. | [optional] [readonly]
**shared_by** | [**\SomeonesComputer\Sdk\Model\User**](User.md) |  | [optional]
**id** | **string** |  | [optional] [readonly]
**created_at** | **\DateTime** |  | [optional] [readonly]
**updated_at** | **\DateTime** |  | [optional] [readonly]
**display_label** | **string** | The reference as it is written for a reader: &#x60;F-24GT1BQ7&#x60;. | [optional] [readonly]
**shared** | **bool** | Whether an unauthenticated request may read this: a token was minted and it has not yet passed its expiry. | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

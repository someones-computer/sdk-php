# # Swarm

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**owner** | **string** | Null for the platform pool; set for a customer BYO cluster. | [optional]
**kind** | **string** |  | [optional] [readonly]
**name** | **string** |  | [optional]
**endpoint** | **string** | Manager API endpoint (tcp+TLS) or SSH target. | [optional]
**status** | **string** |  | [optional] [default to 'unreachable']
**public_host** | **string** | The address a client *outside* the cluster reaches this context&#39;s published ports on — a hostname or an IP, no scheme and no port. | [optional]
**roles** | **string[]** | What this context is used for — builds, runtime, or both. Stored as the enum&#39;s string values rather than a relation: it is a small fixed set, and a json column needs no join to answer \&quot;where can I build?\&quot;. | [optional]
**last_seen_at** | **\DateTime** |  | [optional]
**capacity** | **array<string,string>** | Observed capacity snapshot (cpu/mem/nodes), reconciled from the swarm — whatever {@see \\App\\Service\\Swarm\\SwarmHealth::$capacity} carried at the last successful probe. | [optional]
**labels** | **array<string,string>** |  | [optional] [readonly]
**ingress_installed_at** | **\DateTime** | When {@see \\App\\Service\\Ingress\\TraefikInstaller} last stood up (or confirmed) the edge on this context, dispatched automatically once it becomes a platform-owned runtime context. | [optional] [readonly]
**ingress_error** | **string** | What the last automatic install attempt said, when it failed. Cleared on a success so the row never shows a stale complaint next to a working edge. | [optional] [readonly]
**ingress_network** | **string** | The shared overlay that install put the edge on — the one Traefik&#39;s &#x60;--providers.swarm.network&#x60; names, and therefore the only network a service can be routed from. | [optional] [readonly]
**ingress_verified_at** | **\DateTime** | When the edge was last *observed* routing — the overlay present, the edge service on it, watching it, with a task running ({@see \\App\\Service\\Ingress\\IngressVerifier}). | [optional] [readonly]
**ingress_verification_error** | **string** | What the last verification found wrong, or null when the edge was routing. | [optional] [readonly]
**nodes** | [**\SomeonesComputer\Sdk\Model\SwarmNode[]**](SwarmNode.md) |  | [optional]
**machines** | [**\SomeonesComputer\Sdk\Model\Machine[]**](Machine.md) |  | [optional]
**deployments** | **string[]** | The revisions placed here. Mapped for the same single reason as {@see self::$machines} — so a delete can let go of them — rather than as a collection anything reads; {@see \\App\\Repository\\DeploymentRepository} is where a caller asks what is on a context. | [optional]
**id** | **string** |  | [optional] [readonly]
**deleted_at** | **\DateTime** |  | [optional] [readonly]
**created_at** | **\DateTime** |  | [optional] [readonly]
**updated_at** | **\DateTime** |  | [optional] [readonly]
**platform_owned** | **bool** |  | [optional] [readonly]
**platform_provisioned** | **bool** | Whether the platform itself stood this context up, whoever currently owns the row — a machine {@see \\App\\MessageHandler\\ProvisionMachineHandler} provisioned, running this platform&#39;s own trusted image, versus a customer&#39;s own cluster registered straight through {@see \\App\\Controller\\Admin\\SwarmController}. | [optional] [readonly]
**working_edge** | **bool** | Whether a revision that publishes a port can be routed here. | [optional] [readonly]
**deleted** | **bool** |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

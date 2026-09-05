# # Service

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deployment** | **string** |  | [optional]
**name** | **string** |  | [optional]
**image** | **string** |  | [optional]
**replicas** | **int** |  | [optional] [default to 1]
**cpu_limit** | [**\SomeonesComputer\Sdk\Model\ServiceCpuLimit**](ServiceCpuLimit.md) |  | [optional]
**mem_limit** | [**\SomeonesComputer\Sdk\Model\ServiceMemLimit**](ServiceMemLimit.md) |  | [optional]
**cpu_reservation** | [**\SomeonesComputer\Sdk\Model\ServiceCpuReservation**](ServiceCpuReservation.md) |  | [optional]
**mem_reservation** | [**\SomeonesComputer\Sdk\Model\ServiceMemReservation**](ServiceMemReservation.md) |  | [optional]
**ports** | **array<string,\SomeonesComputer\Sdk\Model\ServicePortsInnerValue>[]** |  | [optional]
**http_port** | **int** | The container port this service speaks HTTP on, as compose&#39;s &#x60;x-someones.http&#x60; declared it — null means nothing was declared and {@see \\App\\Service\\Ingress\\IngressPlanner} falls back to the well-known ports. | [optional]
**command** | **string[]** | The container&#39;s argv, as compose &#x60;command:&#x60; declared it — already split into words by the parser, because Swarm&#39;s &#x60;Args&#x60; is argv rather than a line. | [optional]
**entrypoint** | **string[]** | The container&#39;s &#x60;Command&#x60; — compose &#x60;entrypoint:&#x60;, which replaces the image&#39;s own &#x60;ENTRYPOINT&#x60; rather than feeding it, unlike {@see $command}. | [optional]
**healthcheck** | [**array<string,\SomeonesComputer\Sdk\Model\ServiceHealthcheckValue>**](ServiceHealthcheckValue.md) | Compose &#x60;healthcheck:&#x60;, projected straight from {@see \\App\\Service\\Compose\\ComposeParser::healthcheck()} into the shape {@see \\App\\Service\\Deploy\\StackDeployer} sends as Swarm&#39;s &#x60;ContainerSpec.Healthcheck&#x60; — &#x60;test&#x60; is a &#x60;NONE&#x60;/&#x60;CMD&#x60;/&#x60;CMD-SHELL&#x60; argv, the rest are nanoseconds/a count. Null means nothing was declared, so an image&#39;s own baked-in &#x60;HEALTHCHECK&#x60; (or none) stands; &#x60;disable: true&#x60; in the compose file is not null, it is &#x60;test: [\&quot;NONE\&quot;]&#x60; — an explicit instruction rather than silence. | [optional]
**restart** | **string** | What happens when a container exits; also decides service vs job. | [optional] [default to 'always']
**forwarded_unscanned** | **bool** | Set while this service&#39;s image arrived by client-side forwarding (docs/registry.md&#39;s \&quot;Client-side forwarding\&quot; callout) and no scan verdict is yet on record for the digest it was pinned to — bytes from a user&#39;s machine, not a source tree we built or a registry we chose to trust. A forwarded image is scanned as it loads ({@see \\App\\MessageHandler\\BuildBundleHandler}), so this is normally cleared by the time the service is projected; one left set is a forwarded image that reached deploy unvetted, which {@see \\App\\MessageHandler\\DeployRevisionHandler} refuses to run (docs/image-scanning.md). | [optional] [default to false]
**id** | **string** |  | [optional] [readonly]
**created_at** | **\DateTime** |  | [optional] [readonly]
**updated_at** | **\DateTime** |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

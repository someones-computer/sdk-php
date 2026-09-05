# # CreditTransaction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization** | **string** |  | [optional]
**type** | **string** |  | [optional]
**status** | **string** |  | [optional] [default to 'pending']
**amount_cents** | **int** | Signed integer amount in the smallest currency unit (cents for USD). | [optional]
**currency** | **string** |  | [optional] [default to 'usd']
**stripe_checkout_session_id** | **string** | Stripe Checkout Session id; a top-up row is created Pending against this before redirecting. Null on a grant and on a debit, neither of which has a Stripe session — the *type* is what says which kind of row this is, not whether this column is set. | [optional]
**usage_hour** | **\DateTime** | The clock hour a debit bills for, truncated to the hour and stored UTC. | [optional] [readonly]
**resource_kind** | **string** | Which meter wrote this row; null on every non-debit row. The other half of the unique key above, and always set on a debit — never left null the way a top-up or grant&#39;s &#x60;usageHour&#x60; is, or two debits from different meters in the same hour would stop colliding with each other but a debit from the *same* meter twice would also stop colliding with itself. | [optional] [readonly]
**usage_seconds** | **int** | Resolved container-seconds this debit was computed from; null on anything but a compute debit. | [optional] [readonly]
**unresolved_containers** | **int** | Containers the meter saw start and never saw stop over the billed hour. | [optional] [readonly]
**usage_bytes** | [**\SomeonesComputer\Sdk\Model\CreditTransactionUsageBytes**](CreditTransactionUsageBytes.md) |  | [optional]
**engine_millis** | [**\SomeonesComputer\Sdk\Model\CreditTransactionEngineMillis**](CreditTransactionEngineMillis.md) |  | [optional]
**stripe_event_id** | **string** | Stripe Event id that last transitioned this row; secondary idempotency guard for webhook delivery. | [optional]
**created_by** | [**\SomeonesComputer\Sdk\Model\User**](User.md) |  | [optional]
**id** | **string** |  | [optional] [readonly]
**created_at** | **\DateTime** |  | [optional] [readonly]
**updated_at** | **\DateTime** |  | [optional] [readonly]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)

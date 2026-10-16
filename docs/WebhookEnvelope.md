# WebhookEnvelope

Body of every webhook delivery. Verify `X-Signature` (HMAC-SHA256 of the raw body with the webhook secret) before trusting it, and de-duplicate on `id`. See [Webhooks](/webhooks). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event** | **str** |  | 
**id** | **str** | Delivery ID, one per event. Retries and manual resends repeat it. | 
**occurred_at** | **datetime** | When the event happened (ISO 8601, UTC). | 
**workspace_uuid** | **str** | The workspace the event belongs to (null only on instance-wide system webhooks). Also sent as the &#x60;X-PostBoost-Workspace&#x60; header. | 
**data** | **Dict[str, object]** | The post (&#x60;post.*&#x60;, as &#x60;getPost&#x60; returns it, plus &#x60;account&#x60; on per-account events), the account (&#x60;account.*&#x60;) or the reply draft (&#x60;inbox.*&#x60;). | 

## Example

```python
from postboost.models.webhook_envelope import WebhookEnvelope

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookEnvelope from a JSON string
webhook_envelope_instance = WebhookEnvelope.from_json(json)
# print the JSON string representation of the object
print(WebhookEnvelope.to_json())

# convert the object into a dict
webhook_envelope_dict = webhook_envelope_instance.to_dict()
# create an instance of WebhookEnvelope from a dict
webhook_envelope_from_dict = WebhookEnvelope.from_dict(webhook_envelope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



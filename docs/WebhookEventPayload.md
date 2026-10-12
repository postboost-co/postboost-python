# WebhookEventPayload

Body of every delivery. `data` is the post (post events) or the account (account events).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event** | [**WebhookEventName**](WebhookEventName.md) |  | 
**data** | **Dict[str, object]** |  | 

## Example

```python
from postboost.models.webhook_event_payload import WebhookEventPayload

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookEventPayload from a JSON string
webhook_event_payload_instance = WebhookEventPayload.from_json(json)
# print the JSON string representation of the object
print(WebhookEventPayload.to_json())

# convert the object into a dict
webhook_event_payload_dict = webhook_event_payload_instance.to_dict()
# create an instance of WebhookEventPayload from a dict
webhook_event_payload_from_dict = WebhookEventPayload.from_dict(webhook_event_payload_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



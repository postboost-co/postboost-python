# WebhookSubscriptionInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**callback_url** | **str** | Public &#x60;https://&#x60; URL that receives the deliveries. | 
**events** | [**List[WebhookEventName]**](WebhookEventName.md) |  | 
**name** | **str** | Label shown in Settings → Webhooks. Defaults to \&quot;&lt;Source&gt; trigger\&quot;. | [optional] 
**source** | **str** | The tool creating the subscription. | [optional] 

## Example

```python
from postboost.models.webhook_subscription_input import WebhookSubscriptionInput

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookSubscriptionInput from a JSON string
webhook_subscription_input_instance = WebhookSubscriptionInput.from_json(json)
# print the JSON string representation of the object
print(WebhookSubscriptionInput.to_json())

# convert the object into a dict
webhook_subscription_input_dict = webhook_subscription_input_instance.to_dict()
# create an instance of WebhookSubscriptionInput from a dict
webhook_subscription_input_from_dict = WebhookSubscriptionInput.from_dict(webhook_subscription_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



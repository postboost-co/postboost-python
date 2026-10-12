# CreateWebhookSubscription201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**CreateWebhookSubscription201ResponseData**](CreateWebhookSubscription201ResponseData.md) |  | 

## Example

```python
from postboost.models.create_webhook_subscription201_response import CreateWebhookSubscription201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateWebhookSubscription201Response from a JSON string
create_webhook_subscription201_response_instance = CreateWebhookSubscription201Response.from_json(json)
# print the JSON string representation of the object
print(CreateWebhookSubscription201Response.to_json())

# convert the object into a dict
create_webhook_subscription201_response_dict = create_webhook_subscription201_response_instance.to_dict()
# create an instance of CreateWebhookSubscription201Response from a dict
create_webhook_subscription201_response_from_dict = CreateWebhookSubscription201Response.from_dict(create_webhook_subscription201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# CreateWebhookSubscription201ResponseData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** |  | 
**name** | **str** |  | 
**callback_url** | **str** |  | 
**events** | **List[str]** |  | 
**active** | **bool** |  | 
**created_at** | **datetime** |  | [optional] 
**secret** | **str** | Signing secret for &#x60;X-Signature&#x60;. Returned once. | 

## Example

```python
from postboost.models.create_webhook_subscription201_response_data import CreateWebhookSubscription201ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of CreateWebhookSubscription201ResponseData from a JSON string
create_webhook_subscription201_response_data_instance = CreateWebhookSubscription201ResponseData.from_json(json)
# print the JSON string representation of the object
print(CreateWebhookSubscription201ResponseData.to_json())

# convert the object into a dict
create_webhook_subscription201_response_data_dict = create_webhook_subscription201_response_data_instance.to_dict()
# create an instance of CreateWebhookSubscription201ResponseData from a dict
create_webhook_subscription201_response_data_from_dict = CreateWebhookSubscription201ResponseData.from_dict(create_webhook_subscription201_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# FreeToolVerifyWebhookSignatureResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**valid** | **bool** |  | [optional] 
**expected** | **str** | The signature the body and secret give, with the prefix. | [optional] 
**hints** | **List[str]** | When invalid: the usual mistakes that would make it valid, each checked. | [optional] 

## Example

```python
from postboost.models.free_tool_verify_webhook_signature_response import FreeToolVerifyWebhookSignatureResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolVerifyWebhookSignatureResponse from a JSON string
free_tool_verify_webhook_signature_response_instance = FreeToolVerifyWebhookSignatureResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolVerifyWebhookSignatureResponse.to_json())

# convert the object into a dict
free_tool_verify_webhook_signature_response_dict = free_tool_verify_webhook_signature_response_instance.to_dict()
# create an instance of FreeToolVerifyWebhookSignatureResponse from a dict
free_tool_verify_webhook_signature_response_from_dict = FreeToolVerifyWebhookSignatureResponse.from_dict(free_tool_verify_webhook_signature_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



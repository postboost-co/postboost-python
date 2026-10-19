# FreeToolVerifyWebhookSignatureRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **str** | The raw request body exactly as received (up to 64 KB). Use a test payload, not production data. | 
**secret** | **str** | The webhook secret. Use a test secret: never send a production secret to any third-party service. | 
**signature** | **str** | The received signature header value, e.g. X-Signature. | 
**algorithm** | **str** |  | [optional] [default to 'sha256']
**encoding** | **str** |  | [optional] [default to 'hex']
**prefix** | **str** | A prefix the sender puts before the signature, e.g. \&quot;sha256&#x3D;\&quot; (GitHub). | [optional] [default to '']

## Example

```python
from postboost.models.free_tool_verify_webhook_signature_request import FreeToolVerifyWebhookSignatureRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolVerifyWebhookSignatureRequest from a JSON string
free_tool_verify_webhook_signature_request_instance = FreeToolVerifyWebhookSignatureRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolVerifyWebhookSignatureRequest.to_json())

# convert the object into a dict
free_tool_verify_webhook_signature_request_dict = free_tool_verify_webhook_signature_request_instance.to_dict()
# create an instance of FreeToolVerifyWebhookSignatureRequest from a dict
free_tool_verify_webhook_signature_request_from_dict = FreeToolVerifyWebhookSignatureRequest.from_dict(free_tool_verify_webhook_signature_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



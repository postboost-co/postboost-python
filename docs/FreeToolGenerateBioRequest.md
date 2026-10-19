# FreeToolGenerateBioRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | What you or your brand do, and for whom. | 
**tone** | **str** |  | [optional] [default to 'friendly']
**emoji** | **bool** | Use one or two fitting emoji. | [optional] [default to True]
**cta** | **bool** | End with a short call to action, such as the link in bio. | [optional] [default to True]
**network** | **str** | The network the bio is written for (Instagram for now). | [optional] [default to 'instagram']
**workspace** | **str** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_bio_request import FreeToolGenerateBioRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateBioRequest from a JSON string
free_tool_generate_bio_request_instance = FreeToolGenerateBioRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateBioRequest.to_json())

# convert the object into a dict
free_tool_generate_bio_request_dict = free_tool_generate_bio_request_instance.to_dict()
# create an instance of FreeToolGenerateBioRequest from a dict
free_tool_generate_bio_request_from_dict = FreeToolGenerateBioRequest.from_dict(free_tool_generate_bio_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



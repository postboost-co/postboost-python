# FreeToolGenerateHooksRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**topic** | **str** | What the post is about. | 
**tone** | **str** | Tone of the hooks, as on the caption generator. | [optional] [default to 'friendly']
**count** | **int** | How many hooks to write. | [optional] [default to 5]
**network** | **str** | The network the text is written for. | [optional] [default to 'instagram']
**workspace** | **str** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_hooks_request import FreeToolGenerateHooksRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateHooksRequest from a JSON string
free_tool_generate_hooks_request_instance = FreeToolGenerateHooksRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateHooksRequest.to_json())

# convert the object into a dict
free_tool_generate_hooks_request_dict = free_tool_generate_hooks_request_instance.to_dict()
# create an instance of FreeToolGenerateHooksRequest from a dict
free_tool_generate_hooks_request_from_dict = FreeToolGenerateHooksRequest.from_dict(free_tool_generate_hooks_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



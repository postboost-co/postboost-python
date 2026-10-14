# FreeToolError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**retry_after** | **int** | 429 only: seconds until the limit resets. | [optional] 
**register_url** | **str** | 429 for guests: sign up for a token with higher limits. | [optional] 
**upgrade_url** | **str** | 429 when a token user reached the plan&#39;s daily cap. | [optional] 

## Example

```python
from postboost.models.free_tool_error import FreeToolError

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolError from a JSON string
free_tool_error_instance = FreeToolError.from_json(json)
# print the JSON string representation of the object
print(FreeToolError.to_json())

# convert the object into a dict
free_tool_error_dict = free_tool_error_instance.to_dict()
# create an instance of FreeToolError from a dict
free_tool_error_from_dict = FreeToolError.from_dict(free_tool_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



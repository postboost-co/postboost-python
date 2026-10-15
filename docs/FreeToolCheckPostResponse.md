# FreeToolCheckPostResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**networks** | [**List[FreeToolCheckPostResponseNetworksInner]**](FreeToolCheckPostResponseNetworksInner.md) |  | [optional] 

## Example

```python
from postboost.models.free_tool_check_post_response import FreeToolCheckPostResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCheckPostResponse from a JSON string
free_tool_check_post_response_instance = FreeToolCheckPostResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCheckPostResponse.to_json())

# convert the object into a dict
free_tool_check_post_response_dict = free_tool_check_post_response_instance.to_dict()
# create an instance of FreeToolCheckPostResponse from a dict
free_tool_check_post_response_from_dict = FreeToolCheckPostResponse.from_dict(free_tool_check_post_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



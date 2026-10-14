# FreeToolSplitThreadResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit** | **int** |  | [optional] 
**posts** | [**List[FreeToolSplitThreadResponsePostsInner]**](FreeToolSplitThreadResponsePostsInner.md) |  | [optional] 

## Example

```python
from postboost.models.free_tool_split_thread_response import FreeToolSplitThreadResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolSplitThreadResponse from a JSON string
free_tool_split_thread_response_instance = FreeToolSplitThreadResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolSplitThreadResponse.to_json())

# convert the object into a dict
free_tool_split_thread_response_dict = free_tool_split_thread_response_instance.to_dict()
# create an instance of FreeToolSplitThreadResponse from a dict
free_tool_split_thread_response_from_dict = FreeToolSplitThreadResponse.from_dict(free_tool_split_thread_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



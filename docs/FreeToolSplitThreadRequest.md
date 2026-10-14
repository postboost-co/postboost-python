# FreeToolSplitThreadRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | The long text, up to 10,000 characters. A line with only --- forces a new post. | [optional] [default to '']
**network** | **str** |  | [optional] [default to 'x']
**numbering** | **bool** | End each post with \&quot; k/n\&quot;. | [optional] [default to False]

## Example

```python
from postboost.models.free_tool_split_thread_request import FreeToolSplitThreadRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolSplitThreadRequest from a JSON string
free_tool_split_thread_request_instance = FreeToolSplitThreadRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolSplitThreadRequest.to_json())

# convert the object into a dict
free_tool_split_thread_request_dict = free_tool_split_thread_request_instance.to_dict()
# create an instance of FreeToolSplitThreadRequest from a dict
free_tool_split_thread_request_from_dict = FreeToolSplitThreadRequest.from_dict(free_tool_split_thread_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



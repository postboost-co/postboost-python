# FreeToolGenerateLinkedInHeadlineRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** | Your role or what you do. | 
**skills** | **str** | Your skills and the value you bring. | 
**audience** | **str** | Who you help (optional). | [optional] [default to '']
**tone** | **str** |  | [optional] [default to 'professional']
**workspace** | **str** | UUID of the workspace whose AI credits pay for the call. Default: your active workspace (a scoped API key: its own workspace). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_linked_in_headline_request import FreeToolGenerateLinkedInHeadlineRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateLinkedInHeadlineRequest from a JSON string
free_tool_generate_linked_in_headline_request_instance = FreeToolGenerateLinkedInHeadlineRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateLinkedInHeadlineRequest.to_json())

# convert the object into a dict
free_tool_generate_linked_in_headline_request_dict = free_tool_generate_linked_in_headline_request_instance.to_dict()
# create an instance of FreeToolGenerateLinkedInHeadlineRequest from a dict
free_tool_generate_linked_in_headline_request_from_dict = FreeToolGenerateLinkedInHeadlineRequest.from_dict(free_tool_generate_linked_in_headline_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# FreeToolFormatLinkedInPostResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | [optional] 
**count** | **int** |  | [optional] 
**limit** | **int** |  | [optional] 
**preview** | **str** | What the feed shows before \&quot;…see more\&quot; (about 3 lines or 210 characters; varies by device). | [optional] 
**folded** | **bool** |  | [optional] 

## Example

```python
from postboost.models.free_tool_format_linked_in_post_response import FreeToolFormatLinkedInPostResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolFormatLinkedInPostResponse from a JSON string
free_tool_format_linked_in_post_response_instance = FreeToolFormatLinkedInPostResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolFormatLinkedInPostResponse.to_json())

# convert the object into a dict
free_tool_format_linked_in_post_response_dict = free_tool_format_linked_in_post_response_instance.to_dict()
# create an instance of FreeToolFormatLinkedInPostResponse from a dict
free_tool_format_linked_in_post_response_from_dict = FreeToolFormatLinkedInPostResponse.from_dict(free_tool_format_linked_in_post_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



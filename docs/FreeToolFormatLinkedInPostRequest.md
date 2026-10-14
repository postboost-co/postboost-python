# FreeToolFormatLinkedInPostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**style** | **str** | Unicode style for the whole text, e.g. bold. | [optional] 
**list** | **str** | Prefix every non-empty line with \&quot;• \&quot; or \&quot;1. \&quot;, \&quot;2. \&quot; (plain digits). | [optional] 

## Example

```python
from postboost.models.free_tool_format_linked_in_post_request import FreeToolFormatLinkedInPostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolFormatLinkedInPostRequest from a JSON string
free_tool_format_linked_in_post_request_instance = FreeToolFormatLinkedInPostRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolFormatLinkedInPostRequest.to_json())

# convert the object into a dict
free_tool_format_linked_in_post_request_dict = free_tool_format_linked_in_post_request_instance.to_dict()
# create an instance of FreeToolFormatLinkedInPostRequest from a dict
free_tool_format_linked_in_post_request_from_dict = FreeToolFormatLinkedInPostRequest.from_dict(free_tool_format_linked_in_post_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



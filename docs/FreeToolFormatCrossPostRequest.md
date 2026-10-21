# FreeToolFormatCrossPostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | The post text, up to 10,000 characters. | [optional] [default to '']
**networks** | **List[str]** | The networks to format for, in the order the result lists them. | [optional] [default to [x, threads, bluesky, mastodon, linkedin]]
**numbering** | **bool** | End each post of a thread with \&quot; k/n\&quot;. | [optional] [default to False]

## Example

```python
from postboost.models.free_tool_format_cross_post_request import FreeToolFormatCrossPostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolFormatCrossPostRequest from a JSON string
free_tool_format_cross_post_request_instance = FreeToolFormatCrossPostRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolFormatCrossPostRequest.to_json())

# convert the object into a dict
free_tool_format_cross_post_request_dict = free_tool_format_cross_post_request_instance.to_dict()
# create an instance of FreeToolFormatCrossPostRequest from a dict
free_tool_format_cross_post_request_from_dict = FreeToolFormatCrossPostRequest.from_dict(free_tool_format_cross_post_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



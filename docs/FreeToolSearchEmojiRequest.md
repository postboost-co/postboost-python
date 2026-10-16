# FreeToolSearchEmojiRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **str** | Words to look for in the emoji name and keywords, e.g. &#x60;fire&#x60; or &#x60;party&#x60;. Empty lists the category in Unicode order. | [optional] [default to '']
**category** | **str** | Only emoji of this Unicode category. | [optional] 
**limit** | **int** |  | [optional] [default to 30]

## Example

```python
from postboost.models.free_tool_search_emoji_request import FreeToolSearchEmojiRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolSearchEmojiRequest from a JSON string
free_tool_search_emoji_request_instance = FreeToolSearchEmojiRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolSearchEmojiRequest.to_json())

# convert the object into a dict
free_tool_search_emoji_request_dict = free_tool_search_emoji_request_instance.to_dict()
# create an instance of FreeToolSearchEmojiRequest from a dict
free_tool_search_emoji_request_from_dict = FreeToolSearchEmojiRequest.from_dict(free_tool_search_emoji_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



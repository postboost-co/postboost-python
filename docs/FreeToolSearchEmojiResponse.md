# FreeToolSearchEmojiResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**results** | [**List[FreeToolSearchEmojiResponseResultsInner]**](FreeToolSearchEmojiResponseResultsInner.md) |  | [optional] 
**total** | **int** | Matches before &#x60;limit&#x60;. | [optional] 

## Example

```python
from postboost.models.free_tool_search_emoji_response import FreeToolSearchEmojiResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolSearchEmojiResponse from a JSON string
free_tool_search_emoji_response_instance = FreeToolSearchEmojiResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolSearchEmojiResponse.to_json())

# convert the object into a dict
free_tool_search_emoji_response_dict = free_tool_search_emoji_response_instance.to_dict()
# create an instance of FreeToolSearchEmojiResponse from a dict
free_tool_search_emoji_response_from_dict = FreeToolSearchEmojiResponse.from_dict(free_tool_search_emoji_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



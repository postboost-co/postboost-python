# FreeToolSearchEmojiResponseResultsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**emoji** | **str** |  | [optional] 
**name** | **str** | Unicode name (emoji-test.txt). | [optional] 
**keywords** | **List[str]** | CLDR English keywords. | [optional] 
**category** | **str** |  | [optional] 
**unicode_version** | **str** | Emoji version the emoji was added in (emoji-test.txt, e.g. 0.6 &#x3D; Unicode 6.0, 15.1). | [optional] 

## Example

```python
from postboost.models.free_tool_search_emoji_response_results_inner import FreeToolSearchEmojiResponseResultsInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolSearchEmojiResponseResultsInner from a JSON string
free_tool_search_emoji_response_results_inner_instance = FreeToolSearchEmojiResponseResultsInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolSearchEmojiResponseResultsInner.to_json())

# convert the object into a dict
free_tool_search_emoji_response_results_inner_dict = free_tool_search_emoji_response_results_inner_instance.to_dict()
# create an instance of FreeToolSearchEmojiResponseResultsInner from a dict
free_tool_search_emoji_response_results_inner_from_dict = FreeToolSearchEmojiResponseResultsInner.from_dict(free_tool_search_emoji_response_results_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



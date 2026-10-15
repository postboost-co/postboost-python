# FreeToolCleanTextRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**dashes** | **str** | What replaces an em or en dash between words: \&quot;, \&quot; (comma), \&quot;-\&quot; (hyphen), \&quot; - \&quot; (spaced) or nothing (keep). Number ranges like 2020–2024 always get a hyphen. | [optional] [default to 'comma']
**quotes** | **bool** | Curly quotes and apostrophes to straight ones. | [optional] [default to True]
**invisible** | **bool** | Remove zero-width characters and soft hyphens; turn non-breaking and thin spaces into normal spaces. | [optional] [default to True]
**spaces** | **bool** | Collapse double spaces between words and remove spaces at line ends. | [optional] [default to True]
**ellipsis** | **bool** | The ellipsis character to three dots. | [optional] [default to True]
**markdown** | **bool** | Strip **bold**, __bold__, *italic* and _italic_ markers, keeping the words. | [optional] [default to True]
**flag_phrases** | **bool** | List common AI phrases (e.g. \&quot;delve\&quot;) with their offsets. They are never changed. | [optional] [default to True]

## Example

```python
from postboost.models.free_tool_clean_text_request import FreeToolCleanTextRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCleanTextRequest from a JSON string
free_tool_clean_text_request_instance = FreeToolCleanTextRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCleanTextRequest.to_json())

# convert the object into a dict
free_tool_clean_text_request_dict = free_tool_clean_text_request_instance.to_dict()
# create an instance of FreeToolCleanTextRequest from a dict
free_tool_clean_text_request_from_dict = FreeToolCleanTextRequest.from_dict(free_tool_clean_text_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



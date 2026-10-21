# FreeToolFormatCrossPostResponseNetworksInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | [optional] 
**label** | **str** |  | [optional] 
**limit** | **int** |  | [optional] 
**count** | **int** | Length as the network counts it. | [optional] 
**fits** | **bool** |  | [optional] 
**over_by** | **int** | Characters over the limit; 0 when it fits. | [optional] 
**links** | **int** | Unique http(s) links in the text (trailing punctuation trimmed), as Threads counts them. | [optional] 
**warnings** | [**List[FreeToolCheckPostResponseNetworksInnerErrorsInner]**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: threads_too_many_links, cut_by_fold, mentions_not_portable. | [optional] 
**thread** | [**List[FreeToolFormatCrossPostResponseNetworksInnerThreadInner]**](FreeToolFormatCrossPostResponseNetworksInnerThreadInner.md) | The thread for a text that does not fit (X, Threads, Bluesky, Mastodon); null when it fits or on LinkedIn. | [optional] 

## Example

```python
from postboost.models.free_tool_format_cross_post_response_networks_inner import FreeToolFormatCrossPostResponseNetworksInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolFormatCrossPostResponseNetworksInner from a JSON string
free_tool_format_cross_post_response_networks_inner_instance = FreeToolFormatCrossPostResponseNetworksInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolFormatCrossPostResponseNetworksInner.to_json())

# convert the object into a dict
free_tool_format_cross_post_response_networks_inner_dict = free_tool_format_cross_post_response_networks_inner_instance.to_dict()
# create an instance of FreeToolFormatCrossPostResponseNetworksInner from a dict
free_tool_format_cross_post_response_networks_inner_from_dict = FreeToolFormatCrossPostResponseNetworksInner.from_dict(free_tool_format_cross_post_response_networks_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



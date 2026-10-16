# FreeToolCheckYoutubeThumbnailResponseChecksInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | [optional] 
**label** | **str** |  | [optional] 
**status** | **str** | &#x60;check&#x60;: a format YouTube may accept but does not name. | [optional] 
**detail** | **str** | The value found and the requirement. | [optional] 

## Example

```python
from postboost.models.free_tool_check_youtube_thumbnail_response_checks_inner import FreeToolCheckYoutubeThumbnailResponseChecksInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCheckYoutubeThumbnailResponseChecksInner from a JSON string
free_tool_check_youtube_thumbnail_response_checks_inner_instance = FreeToolCheckYoutubeThumbnailResponseChecksInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolCheckYoutubeThumbnailResponseChecksInner.to_json())

# convert the object into a dict
free_tool_check_youtube_thumbnail_response_checks_inner_dict = free_tool_check_youtube_thumbnail_response_checks_inner_instance.to_dict()
# create an instance of FreeToolCheckYoutubeThumbnailResponseChecksInner from a dict
free_tool_check_youtube_thumbnail_response_checks_inner_from_dict = FreeToolCheckYoutubeThumbnailResponseChecksInner.from_dict(free_tool_check_youtube_thumbnail_response_checks_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# FreeToolCheckYoutubeThumbnailResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ok** | **bool** | False when any check fails. | [optional] 
**checks** | [**List[FreeToolCheckYoutubeThumbnailResponseChecksInner]**](FreeToolCheckYoutubeThumbnailResponseChecksInner.md) |  | [optional] 

## Example

```python
from postboost.models.free_tool_check_youtube_thumbnail_response import FreeToolCheckYoutubeThumbnailResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCheckYoutubeThumbnailResponse from a JSON string
free_tool_check_youtube_thumbnail_response_instance = FreeToolCheckYoutubeThumbnailResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCheckYoutubeThumbnailResponse.to_json())

# convert the object into a dict
free_tool_check_youtube_thumbnail_response_dict = free_tool_check_youtube_thumbnail_response_instance.to_dict()
# create an instance of FreeToolCheckYoutubeThumbnailResponse from a dict
free_tool_check_youtube_thumbnail_response_from_dict = FreeToolCheckYoutubeThumbnailResponse.from_dict(free_tool_check_youtube_thumbnail_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



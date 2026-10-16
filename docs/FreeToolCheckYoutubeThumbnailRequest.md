# FreeToolCheckYoutubeThumbnailRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**width** | **int** | Image width in pixels. | 
**height** | **int** | Image height in pixels. | 
**file_size_bytes** | **int** | File size in bytes. | 
**format** | **str** | MIME type, e.g. &#x60;image/png&#x60; or &#x60;image/jpeg&#x60;. | 

## Example

```python
from postboost.models.free_tool_check_youtube_thumbnail_request import FreeToolCheckYoutubeThumbnailRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCheckYoutubeThumbnailRequest from a JSON string
free_tool_check_youtube_thumbnail_request_instance = FreeToolCheckYoutubeThumbnailRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCheckYoutubeThumbnailRequest.to_json())

# convert the object into a dict
free_tool_check_youtube_thumbnail_request_dict = free_tool_check_youtube_thumbnail_request_instance.to_dict()
# create an instance of FreeToolCheckYoutubeThumbnailRequest from a dict
free_tool_check_youtube_thumbnail_request_from_dict = FreeToolCheckYoutubeThumbnailRequest.from_dict(free_tool_check_youtube_thumbnail_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



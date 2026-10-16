# Media


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Numeric media id, returned as a string (the engine casts it). Use &#x60;uuid&#x60; to address media in the API. | 
**uuid** | **str** |  | 
**name** | **str** |  | 
**mime_type** | **str** |  | 
**type** | **str** |  | 
**url** | **str** |  | 
**thumb_url** | **str** |  | [optional] 
**is_video** | **bool** |  | 
**is_processing** | **bool** | True while an uploaded video is still being converted. | [optional] 
**width** | **int** | Width in pixels, when stored. | [optional] 
**height** | **int** | Height in pixels, when stored. | [optional] 
**duration_ms** | **int** | Video duration in milliseconds; null for images or videos not read yet. | [optional] 
**size** | **int** | File size in bytes. | [optional] 
**alt_text** | **str** |  | [optional] 
**folder** | [**MediaFolderRef**](MediaFolderRef.md) |  | [optional] 
**created_at** | **str** | &#x60;Y-m-d H:i:s&#x60; in UTC (not RFC 3339). | 

## Example

```python
from postboost.models.media import Media

# TODO update the JSON string below
json = "{}"
# create an instance of Media from a JSON string
media_instance = Media.from_json(json)
# print the JSON string representation of the object
print(Media.to_json())

# convert the object into a dict
media_dict = media_instance.to_dict()
# create an instance of Media from a dict
media_from_dict = Media.from_dict(media_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



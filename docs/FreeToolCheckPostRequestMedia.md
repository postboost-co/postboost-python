# FreeToolCheckPostRequestMedia

The attached media, all of one type. Omit for a text-only post.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count** | **int** |  | 
**type** | **str** |  | [optional] [default to 'image']
**duration_s** | **float** | Video length in seconds. | [optional] 

## Example

```python
from postboost.models.free_tool_check_post_request_media import FreeToolCheckPostRequestMedia

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCheckPostRequestMedia from a JSON string
free_tool_check_post_request_media_instance = FreeToolCheckPostRequestMedia.from_json(json)
# print the JSON string representation of the object
print(FreeToolCheckPostRequestMedia.to_json())

# convert the object into a dict
free_tool_check_post_request_media_dict = free_tool_check_post_request_media_instance.to_dict()
# create an instance of FreeToolCheckPostRequestMedia from a dict
free_tool_check_post_request_media_from_dict = FreeToolCheckPostRequestMedia.from_dict(free_tool_check_post_request_media_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# ImageAltTextResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**media_uuid** | **str** |  | 
**alt_text** | **str** |  | 
**credits_used** | **int** |  | 
**credits_remaining** | **int** |  | [optional] 

## Example

```python
from postboost.models.image_alt_text_response import ImageAltTextResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ImageAltTextResponse from a JSON string
image_alt_text_response_instance = ImageAltTextResponse.from_json(json)
# print the JSON string representation of the object
print(ImageAltTextResponse.to_json())

# convert the object into a dict
image_alt_text_response_dict = image_alt_text_response_instance.to_dict()
# create an instance of ImageAltTextResponse from a dict
image_alt_text_response_from_dict = ImageAltTextResponse.from_dict(image_alt_text_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



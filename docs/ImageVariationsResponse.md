# ImageVariationsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**images** | [**List[GeneratedImageItem]**](GeneratedImageItem.md) |  | 
**aspect_ratio** | **str** |  | 
**quality** | **str** |  | 
**credits_used** | **int** |  | 
**credits_remaining** | **int** |  | [optional] 

## Example

```python
from postboost.models.image_variations_response import ImageVariationsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ImageVariationsResponse from a JSON string
image_variations_response_instance = ImageVariationsResponse.from_json(json)
# print the JSON string representation of the object
print(ImageVariationsResponse.to_json())

# convert the object into a dict
image_variations_response_dict = image_variations_response_instance.to_dict()
# create an instance of ImageVariationsResponse from a dict
image_variations_response_from_dict = ImageVariationsResponse.from_dict(image_variations_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



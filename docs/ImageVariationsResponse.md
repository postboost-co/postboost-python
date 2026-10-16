# ImageVariationsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**images** | [**List[Media]**](Media.md) |  | 
**aspect_ratio** | **str** |  | 
**quality** | **str** |  | 
**credits_used** | **int** | Text credits only. 0 while the image credit pool is on; &#x60;count × credit_weight&#x60; when it is switched off. | 
**credits_remaining** | **int** | Text credits left this billing cycle (null &#x3D; no limit). | [optional] 
**image_credits_used** | **int** | Image credits this call spent (1 per image; 0 when the image credit pool is switched off). | 
**image_credits_remaining** | **int** | Image credits left this month (null &#x3D; no limit, or the image credit pool is switched off). | 

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



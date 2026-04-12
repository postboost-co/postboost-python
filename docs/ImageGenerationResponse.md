# ImageGenerationResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**images** | [**List[Media]**](Media.md) |  | 
**prompt_used** | **str** |  | 
**revised_prompt** | **str** |  | [optional] 
**aspect_ratio** | **str** |  | 
**quality** | **str** |  | 
**credits_used** | **int** |  | 
**credits_remaining** | **int** |  | [optional] 

## Example

```python
from postboost.models.image_generation_response import ImageGenerationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ImageGenerationResponse from a JSON string
image_generation_response_instance = ImageGenerationResponse.from_json(json)
# print the JSON string representation of the object
print(ImageGenerationResponse.to_json())

# convert the object into a dict
image_generation_response_dict = image_generation_response_instance.to_dict()
# create an instance of ImageGenerationResponse from a dict
image_generation_response_from_dict = ImageGenerationResponse.from_dict(image_generation_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



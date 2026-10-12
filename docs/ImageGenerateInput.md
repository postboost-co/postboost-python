# ImageGenerateInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**caption** | **str** | Social media caption. Triggers standard mode. Takes priority over prompt. | [optional] 
**platform** | **str** | Required when caption is provided. | [optional] 
**template** | **str** |  | [optional] 
**style** | **str** |  | [optional] 
**brand_voice** | **str** | Free-text tone for the image. When sent, it replaces the stored workspace brand voice for this call. | [optional] 
**use_brand_voice** | **bool** | When &#x60;brand_voice&#x60; is not sent, derive the image tone from the workspace brand voice. Ignored in developer mode (&#x60;prompt&#x60;). | [optional] [default to True]
**custom_instructions** | **str** |  | [optional] 
**prompt** | **str** | Developer escape hatch. Bypasses internal prompt builder. Ignored if caption is present. | [optional] 
**aspect_ratio** | **str** |  | [optional] [default to '1:1']
**count** | **int** |  | [optional] [default to 1]
**quality** | **str** |  | [optional] [default to 'standard']

## Example

```python
from postboost.models.image_generate_input import ImageGenerateInput

# TODO update the JSON string below
json = "{}"
# create an instance of ImageGenerateInput from a JSON string
image_generate_input_instance = ImageGenerateInput.from_json(json)
# print the JSON string representation of the object
print(ImageGenerateInput.to_json())

# convert the object into a dict
image_generate_input_dict = image_generate_input_instance.to_dict()
# create an instance of ImageGenerateInput from a dict
image_generate_input_from_dict = ImageGenerateInput.from_dict(image_generate_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



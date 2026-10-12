# ImagePromptInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**caption** | **str** |  | 
**platform** | **str** |  | 
**template** | **str** |  | [optional] 
**style** | **str** |  | [optional] 
**brand_voice** | **str** | Free-text tone for the image. When sent, it replaces the stored workspace brand voice for this call. | [optional] 
**use_brand_voice** | **bool** | When &#x60;brand_voice&#x60; is not sent, derive the image tone from the workspace brand voice. Ignored in developer mode (&#x60;prompt&#x60;). | [optional] [default to True]
**custom_instructions** | **str** |  | [optional] 

## Example

```python
from postboost.models.image_prompt_input import ImagePromptInput

# TODO update the JSON string below
json = "{}"
# create an instance of ImagePromptInput from a JSON string
image_prompt_input_instance = ImagePromptInput.from_json(json)
# print the JSON string representation of the object
print(ImagePromptInput.to_json())

# convert the object into a dict
image_prompt_input_dict = image_prompt_input_instance.to_dict()
# create an instance of ImagePromptInput from a dict
image_prompt_input_from_dict = ImagePromptInput.from_dict(image_prompt_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



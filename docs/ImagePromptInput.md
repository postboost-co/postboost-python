# ImagePromptInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**caption** | **str** |  | 
**platform** | **str** |  | 
**template** | **str** |  | [optional] 
**style** | **str** |  | [optional] 
**brand_voice** | **str** |  | [optional] 
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



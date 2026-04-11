# ImageVariationsInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**media_uuid** | **str** |  | 
**aspect_ratio** | **str** |  | [optional] [default to '1:1']
**count** | **int** |  | [optional] [default to 1]
**quality** | **str** |  | [optional] [default to 'standard']

## Example

```python
from postboost.models.image_variations_input import ImageVariationsInput

# TODO update the JSON string below
json = "{}"
# create an instance of ImageVariationsInput from a JSON string
image_variations_input_instance = ImageVariationsInput.from_json(json)
# print the JSON string representation of the object
print(ImageVariationsInput.to_json())

# convert the object into a dict
image_variations_input_dict = image_variations_input_instance.to_dict()
# create an instance of ImageVariationsInput from a dict
image_variations_input_from_dict = ImageVariationsInput.from_dict(image_variations_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



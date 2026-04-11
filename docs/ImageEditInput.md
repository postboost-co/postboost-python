# ImageEditInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**media_uuid** | **str** | UUID of the source media item to edit | 
**prompt** | **str** | Describe what to change in the image | 
**mask_uuid** | **str** | UUID of a mask image. Transparent areas will be edited. | [optional] 
**aspect_ratio** | **str** |  | [optional] [default to '1:1']
**count** | **int** |  | [optional] [default to 1]
**quality** | **str** |  | [optional] [default to 'standard']

## Example

```python
from postboost.models.image_edit_input import ImageEditInput

# TODO update the JSON string below
json = "{}"
# create an instance of ImageEditInput from a JSON string
image_edit_input_instance = ImageEditInput.from_json(json)
# print the JSON string representation of the object
print(ImageEditInput.to_json())

# convert the object into a dict
image_edit_input_dict = image_edit_input_instance.to_dict()
# create an instance of ImageEditInput from a dict
image_edit_input_from_dict = ImageEditInput.from_dict(image_edit_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



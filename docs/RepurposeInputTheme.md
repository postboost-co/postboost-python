# RepurposeInputTheme

Slide colours as `#RRGGBB`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**background** | **str** |  | [optional] 
**foreground** | **str** |  | [optional] 
**accent** | **str** |  | [optional] 

## Example

```python
from postboost.models.repurpose_input_theme import RepurposeInputTheme

# TODO update the JSON string below
json = "{}"
# create an instance of RepurposeInputTheme from a JSON string
repurpose_input_theme_instance = RepurposeInputTheme.from_json(json)
# print the JSON string representation of the object
print(RepurposeInputTheme.to_json())

# convert the object into a dict
repurpose_input_theme_dict = repurpose_input_theme_instance.to_dict()
# create an instance of RepurposeInputTheme from a dict
repurpose_input_theme_from_dict = RepurposeInputTheme.from_dict(repurpose_input_theme_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



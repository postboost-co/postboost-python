# TemplateInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**content** | [**List[TemplateInputContentInner]**](TemplateInputContentInner.md) | One item per post in a thread; usually one. | [optional] 

## Example

```python
from postboost.models.template_input import TemplateInput

# TODO update the JSON string below
json = "{}"
# create an instance of TemplateInput from a JSON string
template_input_instance = TemplateInput.from_json(json)
# print the JSON string representation of the object
print(TemplateInput.to_json())

# convert the object into a dict
template_input_dict = template_input_instance.to_dict()
# create an instance of TemplateInput from a dict
template_input_from_dict = TemplateInput.from_dict(template_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



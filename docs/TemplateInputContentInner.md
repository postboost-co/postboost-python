# TemplateInputContentInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **str** |  | [optional] 
**media** | **List[int]** | Media &#x60;id&#x60;s from the media library. | [optional] 

## Example

```python
from postboost.models.template_input_content_inner import TemplateInputContentInner

# TODO update the JSON string below
json = "{}"
# create an instance of TemplateInputContentInner from a JSON string
template_input_content_inner_instance = TemplateInputContentInner.from_json(json)
# print the JSON string representation of the object
print(TemplateInputContentInner.to_json())

# convert the object into a dict
template_input_content_inner_dict = template_input_content_inner_instance.to_dict()
# create an instance of TemplateInputContentInner from a dict
template_input_content_inner_from_dict = TemplateInputContentInner.from_dict(template_input_content_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



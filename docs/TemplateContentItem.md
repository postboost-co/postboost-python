# TemplateContentItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **str** |  | 
**media** | **List[Dict[str, object]]** | Media items from the library (same shape as the media endpoints). | 

## Example

```python
from postboost.models.template_content_item import TemplateContentItem

# TODO update the JSON string below
json = "{}"
# create an instance of TemplateContentItem from a JSON string
template_content_item_instance = TemplateContentItem.from_json(json)
# print the JSON string representation of the object
print(TemplateContentItem.to_json())

# convert the object into a dict
template_content_item_dict = template_content_item_instance.to_dict()
# create an instance of TemplateContentItem from a dict
template_content_item_from_dict = TemplateContentItem.from_dict(template_content_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



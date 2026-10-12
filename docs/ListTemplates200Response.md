# ListTemplates200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**links** | [**PaginationMetaLinks**](PaginationMetaLinks.md) |  | [optional] 
**meta** | [**PaginationMetaMeta**](PaginationMetaMeta.md) |  | [optional] 
**data** | [**List[Template]**](Template.md) |  | 

## Example

```python
from postboost.models.list_templates200_response import ListTemplates200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListTemplates200Response from a JSON string
list_templates200_response_instance = ListTemplates200Response.from_json(json)
# print the JSON string representation of the object
print(ListTemplates200Response.to_json())

# convert the object into a dict
list_templates200_response_dict = list_templates200_response_instance.to_dict()
# create an instance of ListTemplates200Response from a dict
list_templates200_response_from_dict = ListTemplates200Response.from_dict(list_templates200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



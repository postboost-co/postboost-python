# ListTags200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[Tag]**](Tag.md) |  | [optional] 

## Example

```python
from postboost.models.list_tags200_response import ListTags200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListTags200Response from a JSON string
list_tags200_response_instance = ListTags200Response.from_json(json)
# print the JSON string representation of the object
print(ListTags200Response.to_json())

# convert the object into a dict
list_tags200_response_dict = list_tags200_response_instance.to_dict()
# create an instance of ListTags200Response from a dict
list_tags200_response_from_dict = ListTags200Response.from_dict(list_tags200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



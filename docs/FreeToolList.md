# FreeToolList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[FreeToolListItem]**](FreeToolListItem.md) |  | 

## Example

```python
from postboost.models.free_tool_list import FreeToolList

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolList from a JSON string
free_tool_list_instance = FreeToolList.from_json(json)
# print the JSON string representation of the object
print(FreeToolList.to_json())

# convert the object into a dict
free_tool_list_dict = free_tool_list_instance.to_dict()
# create an instance of FreeToolList from a dict
free_tool_list_from_dict = FreeToolList.from_dict(free_tool_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



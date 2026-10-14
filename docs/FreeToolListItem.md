# FreeToolListItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slug** | **str** |  | 
**name** | **str** |  | 
**operation_id** | **str** |  | 
**kind** | **str** |  | 
**limits** | **str** | Limit profile: std, fetch or ai. | 
**page_url** | **str** |  | 
**docs_url** | **str** |  | 

## Example

```python
from postboost.models.free_tool_list_item import FreeToolListItem

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolListItem from a JSON string
free_tool_list_item_instance = FreeToolListItem.from_json(json)
# print the JSON string representation of the object
print(FreeToolListItem.to_json())

# convert the object into a dict
free_tool_list_item_dict = free_tool_list_item_instance.to_dict()
# create an instance of FreeToolListItem from a dict
free_tool_list_item_from_dict = FreeToolListItem.from_dict(free_tool_list_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



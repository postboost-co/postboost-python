# ListRecyclingRules200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[RecyclingRule]**](RecyclingRule.md) |  | 

## Example

```python
from postboost.models.list_recycling_rules200_response import ListRecyclingRules200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListRecyclingRules200Response from a JSON string
list_recycling_rules200_response_instance = ListRecyclingRules200Response.from_json(json)
# print the JSON string representation of the object
print(ListRecyclingRules200Response.to_json())

# convert the object into a dict
list_recycling_rules200_response_dict = list_recycling_rules200_response_instance.to_dict()
# create an instance of ListRecyclingRules200Response from a dict
list_recycling_rules200_response_from_dict = ListRecyclingRules200Response.from_dict(list_recycling_rules200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



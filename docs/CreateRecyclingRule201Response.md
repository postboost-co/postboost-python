# CreateRecyclingRule201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**RecyclingRule**](RecyclingRule.md) |  | 

## Example

```python
from postboost.models.create_recycling_rule201_response import CreateRecyclingRule201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateRecyclingRule201Response from a JSON string
create_recycling_rule201_response_instance = CreateRecyclingRule201Response.from_json(json)
# print the JSON string representation of the object
print(CreateRecyclingRule201Response.to_json())

# convert the object into a dict
create_recycling_rule201_response_dict = create_recycling_rule201_response_instance.to_dict()
# create an instance of CreateRecyclingRule201Response from a dict
create_recycling_rule201_response_from_dict = CreateRecyclingRule201Response.from_dict(create_recycling_rule201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



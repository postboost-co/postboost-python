# PaginationMetaMeta


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current_page** | **int** |  | [optional] 
**var_from** | **int** |  | [optional] 
**last_page** | **int** |  | [optional] 
**per_page** | **int** |  | [optional] 
**to** | **int** |  | [optional] 
**total** | **int** |  | [optional] 

## Example

```python
from postboost.models.pagination_meta_meta import PaginationMetaMeta

# TODO update the JSON string below
json = "{}"
# create an instance of PaginationMetaMeta from a JSON string
pagination_meta_meta_instance = PaginationMetaMeta.from_json(json)
# print the JSON string representation of the object
print(PaginationMetaMeta.to_json())

# convert the object into a dict
pagination_meta_meta_dict = pagination_meta_meta_instance.to_dict()
# create an instance of PaginationMetaMeta from a dict
pagination_meta_meta_from_dict = PaginationMetaMeta.from_dict(pagination_meta_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



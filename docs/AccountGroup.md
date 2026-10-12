# AccountGroup


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**uuid** | **str** |  | 
**name** | **str** |  | 
**account_ids** | **List[int]** |  | 

## Example

```python
from postboost.models.account_group import AccountGroup

# TODO update the JSON string below
json = "{}"
# create an instance of AccountGroup from a JSON string
account_group_instance = AccountGroup.from_json(json)
# print the JSON string representation of the object
print(AccountGroup.to_json())

# convert the object into a dict
account_group_dict = account_group_instance.to_dict()
# create an instance of AccountGroup from a dict
account_group_from_dict = AccountGroup.from_dict(account_group_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



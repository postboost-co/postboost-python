# AccountGroupInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**accounts** | **List[int]** | Account &#x60;id&#x60;s of this workspace. Replaces the group&#39;s accounts. | [optional] 

## Example

```python
from postboost.models.account_group_input import AccountGroupInput

# TODO update the JSON string below
json = "{}"
# create an instance of AccountGroupInput from a JSON string
account_group_input_instance = AccountGroupInput.from_json(json)
# print the JSON string representation of the object
print(AccountGroupInput.to_json())

# convert the object into a dict
account_group_input_dict = account_group_input_instance.to_dict()
# create an instance of AccountGroupInput from a dict
account_group_input_from_dict = AccountGroupInput.from_dict(account_group_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



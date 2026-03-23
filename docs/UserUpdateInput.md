# UserUpdateInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**email** | **str** |  | 
**password** | **str** | Omit or set to null to keep the current password. | [optional] 
**password_confirmation** | **str** |  | [optional] 
**is_admin** | **bool** |  | 

## Example

```python
from postboost.models.user_update_input import UserUpdateInput

# TODO update the JSON string below
json = "{}"
# create an instance of UserUpdateInput from a JSON string
user_update_input_instance = UserUpdateInput.from_json(json)
# print the JSON string representation of the object
print(UserUpdateInput.to_json())

# convert the object into a dict
user_update_input_dict = user_update_input_instance.to_dict()
# create an instance of UserUpdateInput from a dict
user_update_input_from_dict = UserUpdateInput.from_dict(user_update_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



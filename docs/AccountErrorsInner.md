# AccountErrorsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **str** |  | [optional] 
**code** | **str** |  | [optional] 
**message** | **str** |  | [optional] 
**raw** | **object** |  | [optional] 

## Example

```python
from postboost.models.account_errors_inner import AccountErrorsInner

# TODO update the JSON string below
json = "{}"
# create an instance of AccountErrorsInner from a JSON string
account_errors_inner_instance = AccountErrorsInner.from_json(json)
# print the JSON string representation of the object
print(AccountErrorsInner.to_json())

# convert the object into a dict
account_errors_inner_dict = account_errors_inner_instance.to_dict()
# create an instance of AccountErrorsInner from a dict
account_errors_inner_from_dict = AccountErrorsInner.from_dict(account_errors_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# AccountErrorsInnerOneOf


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **str** |  | [optional] 
**code** | **str** |  | [optional] 
**message** | **str** |  | [optional] 
**raw** | **object** |  | [optional] 

## Example

```python
from postboost.models.account_errors_inner_one_of import AccountErrorsInnerOneOf

# TODO update the JSON string below
json = "{}"
# create an instance of AccountErrorsInnerOneOf from a JSON string
account_errors_inner_one_of_instance = AccountErrorsInnerOneOf.from_json(json)
# print the JSON string representation of the object
print(AccountErrorsInnerOneOf.to_json())

# convert the object into a dict
account_errors_inner_one_of_dict = account_errors_inner_one_of_instance.to_dict()
# create an instance of AccountErrorsInnerOneOf from a dict
account_errors_inner_one_of_from_dict = AccountErrorsInnerOneOf.from_dict(account_errors_inner_one_of_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



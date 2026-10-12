# GetAccountHealth200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[AccountHealth]**](AccountHealth.md) |  | 

## Example

```python
from postboost.models.get_account_health200_response import GetAccountHealth200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetAccountHealth200Response from a JSON string
get_account_health200_response_instance = GetAccountHealth200Response.from_json(json)
# print the JSON string representation of the object
print(GetAccountHealth200Response.to_json())

# convert the object into a dict
get_account_health200_response_dict = get_account_health200_response_instance.to_dict()
# create an instance of GetAccountHealth200Response from a dict
get_account_health200_response_from_dict = GetAccountHealth200Response.from_dict(get_account_health200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



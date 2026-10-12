# AccountHealth


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**uuid** | **str** |  | 
**name** | **str** |  | 
**provider** | **str** |  | 
**authorized** | **bool** | False when the account must be reconnected. | 
**has_token** | **bool** | Whether an access token is stored for the account. | 
**healthy** | **bool** | &#x60;authorized&#x60; and &#x60;has_token&#x60;: the account can publish. | 
**daily_cap** | [**AccountHealthDailyCap**](AccountHealthDailyCap.md) |  | 
**connection** | [**AccountConnectionHealth**](AccountConnectionHealth.md) |  | 

## Example

```python
from postboost.models.account_health import AccountHealth

# TODO update the JSON string below
json = "{}"
# create an instance of AccountHealth from a JSON string
account_health_instance = AccountHealth.from_json(json)
# print the JSON string representation of the object
print(AccountHealth.to_json())

# convert the object into a dict
account_health_dict = account_health_instance.to_dict()
# create an instance of AccountHealth from a dict
account_health_from_dict = AccountHealth.from_dict(account_health_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# AccountHealthDailyCap


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit** | **int** | Posts allowed per UTC day for this network. | 
**used_today** | **int** | Scheduled, awaiting-approval and published posts counted for today (UTC). | 

## Example

```python
from postboost.models.account_health_daily_cap import AccountHealthDailyCap

# TODO update the JSON string below
json = "{}"
# create an instance of AccountHealthDailyCap from a JSON string
account_health_daily_cap_instance = AccountHealthDailyCap.from_json(json)
# print the JSON string representation of the object
print(AccountHealthDailyCap.to_json())

# convert the object into a dict
account_health_daily_cap_dict = account_health_daily_cap_instance.to_dict()
# create an instance of AccountHealthDailyCap from a dict
account_health_daily_cap_from_dict = AccountHealthDailyCap.from_dict(account_health_daily_cap_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



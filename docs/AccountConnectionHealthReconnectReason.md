# AccountConnectionHealthReconnectReason

Why the daily token check found the account's token dead, for an account that needs a reconnect; null otherwise. Codes: `meta_190_<subcode>` (Facebook, Instagram), `refresh_expired` (TikTok, Pinterest), `linkedin_revoked`, `linkedin_expired`, `google_revoked` (YouTube). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **str** |  | 
**message** | **str** | The reason in plain language. | 
**found_at** | **datetime** | When the check first found the token dead. | 

## Example

```python
from postboost.models.account_connection_health_reconnect_reason import AccountConnectionHealthReconnectReason

# TODO update the JSON string below
json = "{}"
# create an instance of AccountConnectionHealthReconnectReason from a JSON string
account_connection_health_reconnect_reason_instance = AccountConnectionHealthReconnectReason.from_json(json)
# print the JSON string representation of the object
print(AccountConnectionHealthReconnectReason.to_json())

# convert the object into a dict
account_connection_health_reconnect_reason_dict = account_connection_health_reconnect_reason_instance.to_dict()
# create an instance of AccountConnectionHealthReconnectReason from a dict
account_connection_health_reconnect_reason_from_dict = AccountConnectionHealthReconnectReason.from_dict(account_connection_health_reconnect_reason_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# AccountConnectionHealth

Connection health of an account (todo 27). Never contains token values.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** | &#x60;expired&#x60;: must be reconnected now. &#x60;expiring&#x60;: the connection hits its hard expiry within 7 days. &#x60;failing&#x60;: the latest publish attempt failed. &#x60;healthy&#x60;: none of these.  | 
**expiry_kind** | **str** | What limits the connection: &#x60;access&#x60; (the access token), &#x60;refresh&#x60; (the refresh token), &#x60;expired&#x60;, &#x60;unknown&#x60; (refreshed automatically, no known hard limit) or &#x60;none&#x60; (the network&#39;s connections do not expire on a schedule).  | 
**expires_at** | **datetime** | When the connection stops working unless reconnected; null without a hard expiry. | 
**days_left** | **int** | Whole days until &#x60;expires_at&#x60; (0 &#x3D; less than a day). | 
**refreshable** | **bool** | PostBoost refreshes the token automatically until the hard expiry. | 
**note** | **str** | Plain-language explanation of the prediction. | 
**last_success_at** | **datetime** | When the account last published successfully. | 
**last_error** | **str** | The error of the account&#39;s latest failed publish, shortened to 300 characters. | 
**reconnect_url** | **str** | Where a workspace member reconnects the account. | 

## Example

```python
from postboost.models.account_connection_health import AccountConnectionHealth

# TODO update the JSON string below
json = "{}"
# create an instance of AccountConnectionHealth from a JSON string
account_connection_health_instance = AccountConnectionHealth.from_json(json)
# print the JSON string representation of the object
print(AccountConnectionHealth.to_json())

# convert the object into a dict
account_connection_health_dict = account_connection_health_instance.to_dict()
# create an instance of AccountConnectionHealth from a dict
account_connection_health_from_dict = AccountConnectionHealth.from_dict(account_connection_health_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



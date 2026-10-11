# Account


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**uuid** | **str** |  | 
**name** | **str** |  | 
**username** | **str** |  | 
**image** | **str** |  | [optional] 
**provider** | **str** |  | 
**data** | **object** | Provider-specific metadata. | 
**authorized** | **bool** |  | 
**profile_url** | **str** | Public URL of the account&#39;s profile on the network, when known. | [optional] 
**publish_status** | **str** | Only present when the account is embedded in a post. Publishing state of this account for the post. | [optional] 
**published_parts** | **int** | Only present when the account is embedded in a post. How many parts (for example thread items or a first comment) are live on the network. | [optional] 
**created_at** | **datetime** |  | 

## Example

```python
from postboost.models.account import Account

# TODO update the JSON string below
json = "{}"
# create an instance of Account from a JSON string
account_instance = Account.from_json(json)
# print the JSON string representation of the object
print(Account.to_json())

# convert the object into a dict
account_dict = account_instance.to_dict()
# create an instance of Account from a dict
account_from_dict = Account.from_dict(account_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



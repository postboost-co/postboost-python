# ResellerClient


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** | The client workspace UUID; use it as &#x60;workspaceUuid&#x60; for the client&#39;s own endpoints. | 
**name** | **str** |  | 
**status** | **str** |  | 
**accounts** | **int** |  | 
**accounts_needing_reconnect** | **int** |  | 
**members** | **int** |  | 
**created_at** | **datetime** |  | 
**archived_at** | **datetime** |  | 

## Example

```python
from postboost.models.reseller_client import ResellerClient

# TODO update the JSON string below
json = "{}"
# create an instance of ResellerClient from a JSON string
reseller_client_instance = ResellerClient.from_json(json)
# print the JSON string representation of the object
print(ResellerClient.to_json())

# convert the object into a dict
reseller_client_dict = reseller_client_instance.to_dict()
# create an instance of ResellerClient from a dict
reseller_client_from_dict = ResellerClient.from_dict(reseller_client_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# ResellerClientUsage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**used** | **int** | Active client workspaces. | 
**limit** | **int** | Client workspaces the Reseller plan allows. | 

## Example

```python
from postboost.models.reseller_client_usage import ResellerClientUsage

# TODO update the JSON string below
json = "{}"
# create an instance of ResellerClientUsage from a JSON string
reseller_client_usage_instance = ResellerClientUsage.from_json(json)
# print the JSON string representation of the object
print(ResellerClientUsage.to_json())

# convert the object into a dict
reseller_client_usage_dict = reseller_client_usage_instance.to_dict()
# create an instance of ResellerClientUsage from a dict
reseller_client_usage_from_dict = ResellerClientUsage.from_dict(reseller_client_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



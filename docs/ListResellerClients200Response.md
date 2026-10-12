# ListResellerClients200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[ResellerClient]**](ResellerClient.md) |  | 
**meta** | [**ResellerClientUsage**](ResellerClientUsage.md) |  | 

## Example

```python
from postboost.models.list_reseller_clients200_response import ListResellerClients200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListResellerClients200Response from a JSON string
list_reseller_clients200_response_instance = ListResellerClients200Response.from_json(json)
# print the JSON string representation of the object
print(ListResellerClients200Response.to_json())

# convert the object into a dict
list_reseller_clients200_response_dict = list_reseller_clients200_response_instance.to_dict()
# create an instance of ListResellerClients200Response from a dict
list_reseller_clients200_response_from_dict = ListResellerClients200Response.from_dict(list_reseller_clients200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



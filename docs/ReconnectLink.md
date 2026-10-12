# ReconnectLink


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | Single-use link to forward to the account owner. | 
**expires_at** | **datetime** |  | 
**account_uuid** | **str** |  | 

## Example

```python
from postboost.models.reconnect_link import ReconnectLink

# TODO update the JSON string below
json = "{}"
# create an instance of ReconnectLink from a JSON string
reconnect_link_instance = ReconnectLink.from_json(json)
# print the JSON string representation of the object
print(ReconnectLink.to_json())

# convert the object into a dict
reconnect_link_dict = reconnect_link_instance.to_dict()
# create an instance of ReconnectLink from a dict
reconnect_link_from_dict = ReconnectLink.from_dict(reconnect_link_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



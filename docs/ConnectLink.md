# ConnectLink


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | Single-use link for the signed-in user who created it. Valid 15 minutes. | 
**expires_at** | **datetime** |  | 
**provider** | **str** |  | 

## Example

```python
from postboost.models.connect_link import ConnectLink

# TODO update the JSON string below
json = "{}"
# create an instance of ConnectLink from a JSON string
connect_link_instance = ConnectLink.from_json(json)
# print the JSON string representation of the object
print(ConnectLink.to_json())

# convert the object into a dict
connect_link_dict = connect_link_instance.to_dict()
# create an instance of ConnectLink from a dict
connect_link_from_dict = ConnectLink.from_dict(connect_link_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



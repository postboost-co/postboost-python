# CreateConnectLinkRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider** | **str** | The network to connect, as &#x60;provider&#x60; in the account list. | 

## Example

```python
from postboost.models.create_connect_link_request import CreateConnectLinkRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateConnectLinkRequest from a JSON string
create_connect_link_request_instance = CreateConnectLinkRequest.from_json(json)
# print the JSON string representation of the object
print(CreateConnectLinkRequest.to_json())

# convert the object into a dict
create_connect_link_request_dict = create_connect_link_request_instance.to_dict()
# create an instance of CreateConnectLinkRequest from a dict
create_connect_link_request_from_dict = CreateConnectLinkRequest.from_dict(create_connect_link_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



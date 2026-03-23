# DeletePostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**trash** | **bool** |  | [optional] [default to False]
**delete_mode** | [**DeleteMode**](DeleteMode.md) |  | [optional] [default to DeleteMode.APP_ONLY]

## Example

```python
from postboost.models.delete_post_request import DeletePostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeletePostRequest from a JSON string
delete_post_request_instance = DeletePostRequest.from_json(json)
# print the JSON string representation of the object
print(DeletePostRequest.to_json())

# convert the object into a dict
delete_post_request_dict = delete_post_request_instance.to_dict()
# create an instance of DeletePostRequest from a dict
delete_post_request_from_dict = DeletePostRequest.from_dict(delete_post_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



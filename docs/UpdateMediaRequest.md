# UpdateMediaRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**alt_text** | **str** | Alternative text for accessibility. | 

## Example

```python
from postboost.models.update_media_request import UpdateMediaRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateMediaRequest from a JSON string
update_media_request_instance = UpdateMediaRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateMediaRequest.to_json())

# convert the object into a dict
update_media_request_dict = update_media_request_instance.to_dict()
# create an instance of UpdateMediaRequest from a dict
update_media_request_from_dict = UpdateMediaRequest.from_dict(update_media_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



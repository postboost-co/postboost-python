# AddPostToQueueRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timezone** | **str** | Accepted and validated for consistency with the other scheduling endpoints; queue slots are always taken from the workspace posting schedule. | [optional] 

## Example

```python
from postboost.models.add_post_to_queue_request import AddPostToQueueRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AddPostToQueueRequest from a JSON string
add_post_to_queue_request_instance = AddPostToQueueRequest.from_json(json)
# print the JSON string representation of the object
print(AddPostToQueueRequest.to_json())

# convert the object into a dict
add_post_to_queue_request_dict = add_post_to_queue_request_instance.to_dict()
# create an instance of AddPostToQueueRequest from a dict
add_post_to_queue_request_from_dict = AddPostToQueueRequest.from_dict(add_post_to_queue_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



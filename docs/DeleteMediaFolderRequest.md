# DeleteMediaFolderRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delete_media** | **bool** |  | [optional] [default to False]

## Example

```python
from postboost.models.delete_media_folder_request import DeleteMediaFolderRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteMediaFolderRequest from a JSON string
delete_media_folder_request_instance = DeleteMediaFolderRequest.from_json(json)
# print the JSON string representation of the object
print(DeleteMediaFolderRequest.to_json())

# convert the object into a dict
delete_media_folder_request_dict = delete_media_folder_request_instance.to_dict()
# create an instance of DeleteMediaFolderRequest from a dict
delete_media_folder_request_from_dict = DeleteMediaFolderRequest.from_dict(delete_media_folder_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



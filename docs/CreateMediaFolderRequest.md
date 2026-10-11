# CreateMediaFolderRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Folder name; must be unique among its siblings (case-insensitive). | 
**parent** | **str** | UUID of the parent folder, or null for the top level. Folders nest to a limited depth. | [optional] 

## Example

```python
from postboost.models.create_media_folder_request import CreateMediaFolderRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateMediaFolderRequest from a JSON string
create_media_folder_request_instance = CreateMediaFolderRequest.from_json(json)
# print the JSON string representation of the object
print(CreateMediaFolderRequest.to_json())

# convert the object into a dict
create_media_folder_request_dict = create_media_folder_request_instance.to_dict()
# create an instance of CreateMediaFolderRequest from a dict
create_media_folder_request_from_dict = CreateMediaFolderRequest.from_dict(create_media_folder_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



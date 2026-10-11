# MediaFolderInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Folder name; must be unique among its siblings (case-insensitive). | [optional] 
**parent** | **str** | UUID of the parent folder, or null for the top level. Folders nest to a limited depth. | [optional] 

## Example

```python
from postboost.models.media_folder_input import MediaFolderInput

# TODO update the JSON string below
json = "{}"
# create an instance of MediaFolderInput from a JSON string
media_folder_input_instance = MediaFolderInput.from_json(json)
# print the JSON string representation of the object
print(MediaFolderInput.to_json())

# convert the object into a dict
media_folder_input_dict = media_folder_input_instance.to_dict()
# create an instance of MediaFolderInput from a dict
media_folder_input_from_dict = MediaFolderInput.from_dict(media_folder_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



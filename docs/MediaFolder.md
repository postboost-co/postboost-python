# MediaFolder


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** |  | 
**name** | **str** |  | 
**parent** | **str** | UUID of the parent folder; null for a top-level folder. | 
**media_count** | **int** | Media filed anywhere below the folder, including its sub-folders. | 

## Example

```python
from postboost.models.media_folder import MediaFolder

# TODO update the JSON string below
json = "{}"
# create an instance of MediaFolder from a JSON string
media_folder_instance = MediaFolder.from_json(json)
# print the JSON string representation of the object
print(MediaFolder.to_json())

# convert the object into a dict
media_folder_dict = media_folder_instance.to_dict()
# create an instance of MediaFolder from a dict
media_folder_from_dict = MediaFolder.from_dict(media_folder_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# MediaBase64Input


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | **str** | The file as base64. A &#x60;data:&lt;mime&gt;;base64,&#x60; prefix is accepted. At most 20 MB once decoded. | 
**filename** | **str** | File name with extension, for example &#x60;cover.png&#x60;. No folders. | 
**alt_text** | **str** | Alternative text for accessibility. | [optional] 
**folder** | **str** | UUID of the media folder to file the upload in. Omit or null for the library root. | [optional] 

## Example

```python
from postboost.models.media_base64_input import MediaBase64Input

# TODO update the JSON string below
json = "{}"
# create an instance of MediaBase64Input from a JSON string
media_base64_input_instance = MediaBase64Input.from_json(json)
# print the JSON string representation of the object
print(MediaBase64Input.to_json())

# convert the object into a dict
media_base64_input_dict = media_base64_input_instance.to_dict()
# create an instance of MediaBase64Input from a dict
media_base64_input_from_dict = MediaBase64Input.from_dict(media_base64_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



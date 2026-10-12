# RepurposeResultMedia

Source image attached instead of a carousel, when there are no slides.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | [optional] 
**url** | **str** |  | [optional] 

## Example

```python
from postboost.models.repurpose_result_media import RepurposeResultMedia

# TODO update the JSON string below
json = "{}"
# create an instance of RepurposeResultMedia from a JSON string
repurpose_result_media_instance = RepurposeResultMedia.from_json(json)
# print the JSON string representation of the object
print(RepurposeResultMedia.to_json())

# convert the object into a dict
repurpose_result_media_dict = repurpose_result_media_instance.to_dict()
# create an instance of RepurposeResultMedia from a dict
repurpose_result_media_from_dict = RepurposeResultMedia.from_dict(repurpose_result_media_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



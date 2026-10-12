# RepurposeSlide


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**media_id** | **int** | Media library ID; reuse it in post versions. | 
**url** | **str** | Public URL of the image. | 

## Example

```python
from postboost.models.repurpose_slide import RepurposeSlide

# TODO update the JSON string below
json = "{}"
# create an instance of RepurposeSlide from a JSON string
repurpose_slide_instance = RepurposeSlide.from_json(json)
# print the JSON string representation of the object
print(RepurposeSlide.to_json())

# convert the object into a dict
repurpose_slide_dict = repurpose_slide_instance.to_dict()
# create an instance of RepurposeSlide from a dict
repurpose_slide_from_dict = RepurposeSlide.from_dict(repurpose_slide_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



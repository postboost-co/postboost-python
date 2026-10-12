# RepurposeResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source** | [**RepurposeResultSource**](RepurposeResultSource.md) |  | 
**captions** | [**List[BlogToSocialCaption]**](BlogToSocialCaption.md) |  | 
**slides** | [**List[RepurposeSlide]**](RepurposeSlide.md) | Carousel slides in order (hook first, call to action last). Empty without a carousel. | 
**media** | [**RepurposeResultMedia**](RepurposeResultMedia.md) |  | [optional] 
**post_uuid** | **str** | The draft post; null when &#x60;create_post&#x60; was false. | 
**credits_used** | **int** |  | 
**credits_remaining** | **int** | Null for unlimited plans. | 
**warnings** | **List[str]** | Parts that were skipped (for example a network that gets no carousel). | 

## Example

```python
from postboost.models.repurpose_result import RepurposeResult

# TODO update the JSON string below
json = "{}"
# create an instance of RepurposeResult from a JSON string
repurpose_result_instance = RepurposeResult.from_json(json)
# print the JSON string representation of the object
print(RepurposeResult.to_json())

# convert the object into a dict
repurpose_result_dict = repurpose_result_instance.to_dict()
# create an instance of RepurposeResult from a dict
repurpose_result_from_dict = RepurposeResult.from_dict(repurpose_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



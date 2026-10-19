# FreeToolPickSocialMediaToolResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**needs** | **List[str]** | The needs matched, deduplicated, in a fixed order. | [optional] 
**results** | [**List[FreeToolPickSocialMediaToolResponseResultsInner]**](FreeToolPickSocialMediaToolResponseResultsInner.md) | Every tool compared, PostBoost included: by score (highest first), then name. | [optional] 
**checked_at** | **date** | Date of the comparison data snapshot. | [optional] 
**checked_label** | **str** | The snapshot month, as shown on the page. | [optional] 

## Example

```python
from postboost.models.free_tool_pick_social_media_tool_response import FreeToolPickSocialMediaToolResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPickSocialMediaToolResponse from a JSON string
free_tool_pick_social_media_tool_response_instance = FreeToolPickSocialMediaToolResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolPickSocialMediaToolResponse.to_json())

# convert the object into a dict
free_tool_pick_social_media_tool_response_dict = free_tool_pick_social_media_tool_response_instance.to_dict()
# create an instance of FreeToolPickSocialMediaToolResponse from a dict
free_tool_pick_social_media_tool_response_from_dict = FreeToolPickSocialMediaToolResponse.from_dict(free_tool_pick_social_media_tool_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



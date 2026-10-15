# FreeToolCheckPostResponseNetworksInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | [optional] 
**label** | **str** |  | [optional] 
**ok** | **bool** | False when an error would stop the post from publishing. | [optional] 
**count** | **int** | Characters as this network counts them. | [optional] 
**limit** | **int** |  | [optional] 
**errors** | [**List[FreeToolCheckPostResponseNetworksInnerErrorsInner]**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: too_long, too_many_hashtags, media_required, too_many_media, media_type, video_too_long, video_too_short. | [optional] 
**warnings** | [**List[FreeToolCheckPostResponseNetworksInnerErrorsInner]**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: cut_by_fold, link_not_clickable. | [optional] 

## Example

```python
from postboost.models.free_tool_check_post_response_networks_inner import FreeToolCheckPostResponseNetworksInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCheckPostResponseNetworksInner from a JSON string
free_tool_check_post_response_networks_inner_instance = FreeToolCheckPostResponseNetworksInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolCheckPostResponseNetworksInner.to_json())

# convert the object into a dict
free_tool_check_post_response_networks_inner_dict = free_tool_check_post_response_networks_inner_instance.to_dict()
# create an instance of FreeToolCheckPostResponseNetworksInner from a dict
free_tool_check_post_response_networks_inner_from_dict = FreeToolCheckPostResponseNetworksInner.from_dict(free_tool_check_post_response_networks_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



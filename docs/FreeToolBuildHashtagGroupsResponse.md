# FreeToolBuildHashtagGroupsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hashtags** | **List[str]** | Clean hashtags in input order, duplicates removed. | [optional] 
**removed** | [**List[FreeToolBuildHashtagGroupsResponseRemovedInner]**](FreeToolBuildHashtagGroupsResponseRemovedInner.md) | Entries that were dropped, with the reason. | [optional] 
**cap** | **int** | Hashtags PostBoost allows per post on the network; null &#x3D; no hard limit. | [optional] 
**group_size** | **int** | Hashtags per group that was used. | [optional] 
**groups** | [**List[FreeToolBuildHashtagGroupsResponseGroupsInner]**](FreeToolBuildHashtagGroupsResponseGroupsInner.md) |  | [optional] 
**over_cap** | **bool** | A group holds more hashtags than the cap. | [optional] 

## Example

```python
from postboost.models.free_tool_build_hashtag_groups_response import FreeToolBuildHashtagGroupsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolBuildHashtagGroupsResponse from a JSON string
free_tool_build_hashtag_groups_response_instance = FreeToolBuildHashtagGroupsResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolBuildHashtagGroupsResponse.to_json())

# convert the object into a dict
free_tool_build_hashtag_groups_response_dict = free_tool_build_hashtag_groups_response_instance.to_dict()
# create an instance of FreeToolBuildHashtagGroupsResponse from a dict
free_tool_build_hashtag_groups_response_from_dict = FreeToolBuildHashtagGroupsResponse.from_dict(free_tool_build_hashtag_groups_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



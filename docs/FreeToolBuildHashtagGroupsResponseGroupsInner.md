# FreeToolBuildHashtagGroupsResponseGroupsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tags** | **List[str]** |  | [optional] 
**text** | **str** | Ready to paste. | [optional] 
**characters** | **int** | Characters of text, counted like the PostBoost composer. | [optional] 

## Example

```python
from postboost.models.free_tool_build_hashtag_groups_response_groups_inner import FreeToolBuildHashtagGroupsResponseGroupsInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolBuildHashtagGroupsResponseGroupsInner from a JSON string
free_tool_build_hashtag_groups_response_groups_inner_instance = FreeToolBuildHashtagGroupsResponseGroupsInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolBuildHashtagGroupsResponseGroupsInner.to_json())

# convert the object into a dict
free_tool_build_hashtag_groups_response_groups_inner_dict = free_tool_build_hashtag_groups_response_groups_inner_instance.to_dict()
# create an instance of FreeToolBuildHashtagGroupsResponseGroupsInner from a dict
free_tool_build_hashtag_groups_response_groups_inner_from_dict = FreeToolBuildHashtagGroupsResponseGroupsInner.from_dict(free_tool_build_hashtag_groups_response_groups_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



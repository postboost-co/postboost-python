# FreeToolBuildHashtagGroupsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | Hashtags or words, separated by spaces, commas or new lines. A missing # is added. | 
**network** | **str** | Network whose hashtag cap applies. | [optional] [default to 'instagram']
**group_size** | **int** | Hashtags per group. Default: the network&#39;s cap, or 5 when it has no hard cap. | [optional] 
**case** | **str** | keep the first spelling of each hashtag, or lower-case all of them. | [optional] [default to 'keep']
**format** | **str** | inline: one line of tags. first_comment: five \&quot;.\&quot; lines, then the tags. | [optional] [default to 'inline']

## Example

```python
from postboost.models.free_tool_build_hashtag_groups_request import FreeToolBuildHashtagGroupsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolBuildHashtagGroupsRequest from a JSON string
free_tool_build_hashtag_groups_request_instance = FreeToolBuildHashtagGroupsRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolBuildHashtagGroupsRequest.to_json())

# convert the object into a dict
free_tool_build_hashtag_groups_request_dict = free_tool_build_hashtag_groups_request_instance.to_dict()
# create an instance of FreeToolBuildHashtagGroupsRequest from a dict
free_tool_build_hashtag_groups_request_from_dict = FreeToolBuildHashtagGroupsRequest.from_dict(free_tool_build_hashtag_groups_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



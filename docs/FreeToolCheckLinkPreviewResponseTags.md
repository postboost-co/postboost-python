# FreeToolCheckLinkPreviewResponseTags

The preview tags found on the page; null when missing.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ogtitle** | **str** |  | [optional] 
**ogdescription** | **str** |  | [optional] 
**ogimage** | **str** |  | [optional] 
**ogimagewidth** | **str** |  | [optional] 
**ogimageheight** | **str** |  | [optional] 
**ogurl** | **str** |  | [optional] 
**ogtype** | **str** |  | [optional] 
**ogsite_name** | **str** |  | [optional] 
**twittercard** | **str** |  | [optional] 
**twittertitle** | **str** |  | [optional] 
**twitterdescription** | **str** |  | [optional] 
**twitterimage** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**canonical** | **str** |  | [optional] 
**robots** | **str** |  | [optional] 

## Example

```python
from postboost.models.free_tool_check_link_preview_response_tags import FreeToolCheckLinkPreviewResponseTags

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCheckLinkPreviewResponseTags from a JSON string
free_tool_check_link_preview_response_tags_instance = FreeToolCheckLinkPreviewResponseTags.from_json(json)
# print the JSON string representation of the object
print(FreeToolCheckLinkPreviewResponseTags.to_json())

# convert the object into a dict
free_tool_check_link_preview_response_tags_dict = free_tool_check_link_preview_response_tags_instance.to_dict()
# create an instance of FreeToolCheckLinkPreviewResponseTags from a dict
free_tool_check_link_preview_response_tags_from_dict = FreeToolCheckLinkPreviewResponseTags.from_dict(free_tool_check_link_preview_response_tags_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



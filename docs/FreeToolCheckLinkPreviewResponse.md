# FreeToolCheckLinkPreviewResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**final_url** | **str** | The URL after redirects. | [optional] 
**status** | **int** | HTTP status of the final response. | [optional] 
**redirects** | [**List[FreeToolCheckLinkPreviewResponseRedirectsInner]**](FreeToolCheckLinkPreviewResponseRedirectsInner.md) |  | [optional] 
**content_type** | **str** |  | [optional] 
**tags** | [**FreeToolCheckLinkPreviewResponseTags**](FreeToolCheckLinkPreviewResponseTags.md) |  | [optional] 
**image** | [**FreeToolCheckLinkPreviewResponseImage**](FreeToolCheckLinkPreviewResponseImage.md) |  | [optional] 
**previews** | [**Dict[str, FreeToolCheckLinkPreviewResponsePreviewsValue]**](FreeToolCheckLinkPreviewResponsePreviewsValue.md) | The card each network would show. | [optional] 
**warnings** | **List[str]** |  | [optional] 

## Example

```python
from postboost.models.free_tool_check_link_preview_response import FreeToolCheckLinkPreviewResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCheckLinkPreviewResponse from a JSON string
free_tool_check_link_preview_response_instance = FreeToolCheckLinkPreviewResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCheckLinkPreviewResponse.to_json())

# convert the object into a dict
free_tool_check_link_preview_response_dict = free_tool_check_link_preview_response_instance.to_dict()
# create an instance of FreeToolCheckLinkPreviewResponse from a dict
free_tool_check_link_preview_response_from_dict = FreeToolCheckLinkPreviewResponse.from_dict(free_tool_check_link_preview_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



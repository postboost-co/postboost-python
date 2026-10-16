# FreeToolCheckLinkPreviewRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | The public http(s) page to check. | 

## Example

```python
from postboost.models.free_tool_check_link_preview_request import FreeToolCheckLinkPreviewRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCheckLinkPreviewRequest from a JSON string
free_tool_check_link_preview_request_instance = FreeToolCheckLinkPreviewRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCheckLinkPreviewRequest.to_json())

# convert the object into a dict
free_tool_check_link_preview_request_dict = free_tool_check_link_preview_request_instance.to_dict()
# create an instance of FreeToolCheckLinkPreviewRequest from a dict
free_tool_check_link_preview_request_from_dict = FreeToolCheckLinkPreviewRequest.from_dict(free_tool_check_link_preview_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



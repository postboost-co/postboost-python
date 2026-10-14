# FreeToolBuildUtmUrlRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | The http(s) page URL. | 
**utm_source** | **str** |  | [optional] 
**utm_medium** | **str** |  | [optional] 
**utm_campaign** | **str** |  | [optional] 
**utm_term** | **str** |  | [optional] 
**utm_content** | **str** |  | [optional] 
**utm_id** | **str** |  | [optional] 

## Example

```python
from postboost.models.free_tool_build_utm_url_request import FreeToolBuildUtmUrlRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolBuildUtmUrlRequest from a JSON string
free_tool_build_utm_url_request_instance = FreeToolBuildUtmUrlRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolBuildUtmUrlRequest.to_json())

# convert the object into a dict
free_tool_build_utm_url_request_dict = free_tool_build_utm_url_request_instance.to_dict()
# create an instance of FreeToolBuildUtmUrlRequest from a dict
free_tool_build_utm_url_request_from_dict = FreeToolBuildUtmUrlRequest.from_dict(free_tool_build_utm_url_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



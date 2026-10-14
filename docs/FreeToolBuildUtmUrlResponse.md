# FreeToolBuildUtmUrlResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | [optional] 
**warnings** | **List[str]** | Missing GA4 keys and values with capitals, spaces or mixed - and _. | [optional] 

## Example

```python
from postboost.models.free_tool_build_utm_url_response import FreeToolBuildUtmUrlResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolBuildUtmUrlResponse from a JSON string
free_tool_build_utm_url_response_instance = FreeToolBuildUtmUrlResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolBuildUtmUrlResponse.to_json())

# convert the object into a dict
free_tool_build_utm_url_response_dict = free_tool_build_utm_url_response_instance.to_dict()
# create an instance of FreeToolBuildUtmUrlResponse from a dict
free_tool_build_utm_url_response_from_dict = FreeToolBuildUtmUrlResponse.from_dict(free_tool_build_utm_url_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# FreeToolGetSafeZonesRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **str** | The app the vertical video is posted to. Approximate: platforms do not publish official overlay sizes for organic posts, and the UI varies by device and app version. The boxes come from each platform&#39;s guidance for vertical video ads. Sources last verified 2026-10-19. | 
**width** | **int** | Frame width in pixels. The boxes are measured on 1080 × 1920 and scaled to the frame. | [optional] [default to 1080]
**height** | **int** | Frame height in pixels. | [optional] [default to 1920]

## Example

```python
from postboost.models.free_tool_get_safe_zones_request import FreeToolGetSafeZonesRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetSafeZonesRequest from a JSON string
free_tool_get_safe_zones_request_instance = FreeToolGetSafeZonesRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetSafeZonesRequest.to_json())

# convert the object into a dict
free_tool_get_safe_zones_request_dict = free_tool_get_safe_zones_request_instance.to_dict()
# create an instance of FreeToolGetSafeZonesRequest from a dict
free_tool_get_safe_zones_request_from_dict = FreeToolGetSafeZonesRequest.from_dict(free_tool_get_safe_zones_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# FreeToolGetSafeZonesResponse

Approximate: platforms do not publish official overlay sizes for organic posts, and the UI varies by device and app version. The boxes come from each platform's guidance for vertical video ads.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **str** |  | [optional] 
**label** | **str** | Platform name. | [optional] 
**width** | **int** |  | [optional] 
**height** | **int** |  | [optional] 
**unsafe_areas** | [**List[FreeToolGetSafeZonesResponseUnsafeAreasInner]**](FreeToolGetSafeZonesResponseUnsafeAreasInner.md) | Areas the app&#39;s UI usually covers, in frame pixels from the top-left corner. Edges are scaled from 1080 × 1920 and rounded to the nearest pixel (halves up), so neighbouring boxes stay edge to edge. | [optional] 
**safe_area** | [**FreeToolGetSafeZonesResponseSafeArea**](FreeToolGetSafeZonesResponseSafeArea.md) |  | [optional] 
**source** | [**FreeToolGetSafeZonesResponseSource**](FreeToolGetSafeZonesResponseSource.md) |  | [optional] 
**last_verified** | **str** | Date the sources were last checked (YYYY-MM-DD). | [optional] 
**caveat** | **str** |  | [optional] 
**warnings** | **List[str]** | Set when the frame is not 9:16, so the boxes are stretched. | [optional] 

## Example

```python
from postboost.models.free_tool_get_safe_zones_response import FreeToolGetSafeZonesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetSafeZonesResponse from a JSON string
free_tool_get_safe_zones_response_instance = FreeToolGetSafeZonesResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetSafeZonesResponse.to_json())

# convert the object into a dict
free_tool_get_safe_zones_response_dict = free_tool_get_safe_zones_response_instance.to_dict()
# create an instance of FreeToolGetSafeZonesResponse from a dict
free_tool_get_safe_zones_response_from_dict = FreeToolGetSafeZonesResponse.from_dict(free_tool_get_safe_zones_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



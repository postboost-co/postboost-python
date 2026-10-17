# FreeToolGetSafeZonesResponseSource

Where the numbers come from.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | **str** |  | [optional] 
**url** | **str** |  | [optional] 
**basis** | **str** | How the numbers were derived from the source. | [optional] 

## Example

```python
from postboost.models.free_tool_get_safe_zones_response_source import FreeToolGetSafeZonesResponseSource

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetSafeZonesResponseSource from a JSON string
free_tool_get_safe_zones_response_source_instance = FreeToolGetSafeZonesResponseSource.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetSafeZonesResponseSource.to_json())

# convert the object into a dict
free_tool_get_safe_zones_response_source_dict = free_tool_get_safe_zones_response_source_instance.to_dict()
# create an instance of FreeToolGetSafeZonesResponseSource from a dict
free_tool_get_safe_zones_response_source_from_dict = FreeToolGetSafeZonesResponseSource.from_dict(free_tool_get_safe_zones_response_source_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



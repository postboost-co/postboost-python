# FreeToolListAwarenessDaysResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**covers** | [**FreeToolListAwarenessDaysResponseCovers**](FreeToolListAwarenessDaysResponseCovers.md) |  | [optional] 
**total** | **int** | Number of entries returned. | [optional] 
**entries** | [**List[FreeToolListAwarenessDaysResponseEntriesInner]**](FreeToolListAwarenessDaysResponseEntriesInner.md) |  | [optional] 
**last_verified** | **date** | When the data was last checked against its sources. | [optional] 
**sources** | [**List[FreeToolGetImageSizesResponseSourcesInner]**](FreeToolGetImageSizesResponseSourcesInner.md) | Sources of the whole dataset (rows may name their own). | [optional] 

## Example

```python
from postboost.models.free_tool_list_awareness_days_response import FreeToolListAwarenessDaysResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolListAwarenessDaysResponse from a JSON string
free_tool_list_awareness_days_response_instance = FreeToolListAwarenessDaysResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolListAwarenessDaysResponse.to_json())

# convert the object into a dict
free_tool_list_awareness_days_response_dict = free_tool_list_awareness_days_response_instance.to_dict()
# create an instance of FreeToolListAwarenessDaysResponse from a dict
free_tool_list_awareness_days_response_from_dict = FreeToolListAwarenessDaysResponse.from_dict(free_tool_list_awareness_days_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



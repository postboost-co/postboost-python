# FreeToolListAwarenessDaysResponseEntriesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Name of the holiday or observance. | [optional] 
**type** | **str** | Entry type. | [optional] 
**var_date** | **date** | The day, or the first day of a week or month. | [optional] 
**end** | **date** | Last day of a week or month (inclusive); null for a single day. | [optional] 
**countries** | **List[str]** | Country codes, or &#x60;global&#x60;. | [optional] 
**topics** | **List[str]** | Topics. | [optional] 
**source** | **str** | Official or organiser page the date comes from. | [optional] 
**note** | **str** | Regional scope or a day off that differs from the date. | [optional] 
**idea** | **str** | A one-line post idea. | [optional] 

## Example

```python
from postboost.models.free_tool_list_awareness_days_response_entries_inner import FreeToolListAwarenessDaysResponseEntriesInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolListAwarenessDaysResponseEntriesInner from a JSON string
free_tool_list_awareness_days_response_entries_inner_instance = FreeToolListAwarenessDaysResponseEntriesInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolListAwarenessDaysResponseEntriesInner.to_json())

# convert the object into a dict
free_tool_list_awareness_days_response_entries_inner_dict = free_tool_list_awareness_days_response_entries_inner_instance.to_dict()
# create an instance of FreeToolListAwarenessDaysResponseEntriesInner from a dict
free_tool_list_awareness_days_response_entries_inner_from_dict = FreeToolListAwarenessDaysResponseEntriesInner.from_dict(free_tool_list_awareness_days_response_entries_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# FreeToolPlanContentCalendarResponseSlotsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **str** | YYYY-MM-DD | [optional] 
**weekday** | **str** |  | [optional] 
**time** | **str** | HH:MM, local time | [optional] 
**network** | **str** |  | [optional] 
**network_label** | **str** |  | [optional] 
**pillar** | **str** | Empty when no pillars were given. | [optional] 

## Example

```python
from postboost.models.free_tool_plan_content_calendar_response_slots_inner import FreeToolPlanContentCalendarResponseSlotsInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPlanContentCalendarResponseSlotsInner from a JSON string
free_tool_plan_content_calendar_response_slots_inner_instance = FreeToolPlanContentCalendarResponseSlotsInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolPlanContentCalendarResponseSlotsInner.to_json())

# convert the object into a dict
free_tool_plan_content_calendar_response_slots_inner_dict = free_tool_plan_content_calendar_response_slots_inner_instance.to_dict()
# create an instance of FreeToolPlanContentCalendarResponseSlotsInner from a dict
free_tool_plan_content_calendar_response_slots_inner_from_dict = FreeToolPlanContentCalendarResponseSlotsInner.from_dict(free_tool_plan_content_calendar_response_slots_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



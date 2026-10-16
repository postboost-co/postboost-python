# FreeToolPlanContentCalendarResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**end_date** | **str** | Last day of the calendar (YYYY-MM-DD). | [optional] 
**total** | **int** | Number of posts planned. | [optional] 
**slots** | [**List[FreeToolPlanContentCalendarResponseSlotsInner]**](FreeToolPlanContentCalendarResponseSlotsInner.md) |  | [optional] 
**csv** | **str** | The calendar as CSV (UTF-8 with BOM): Date, Day, Time, Network, Pillar, Idea. | [optional] 
**ics** | **str** | The calendar as an iCalendar file: one 15-minute event per post, in floating local time. | [optional] 

## Example

```python
from postboost.models.free_tool_plan_content_calendar_response import FreeToolPlanContentCalendarResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPlanContentCalendarResponse from a JSON string
free_tool_plan_content_calendar_response_instance = FreeToolPlanContentCalendarResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolPlanContentCalendarResponse.to_json())

# convert the object into a dict
free_tool_plan_content_calendar_response_dict = free_tool_plan_content_calendar_response_instance.to_dict()
# create an instance of FreeToolPlanContentCalendarResponse from a dict
free_tool_plan_content_calendar_response_from_dict = FreeToolPlanContentCalendarResponse.from_dict(free_tool_plan_content_calendar_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



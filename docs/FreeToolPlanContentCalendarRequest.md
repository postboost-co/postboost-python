# FreeToolPlanContentCalendarRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**start_date** | **str** | First day of the calendar (YYYY-MM-DD). Each week starts on this weekday. | 
**weeks** | **int** |  | [optional] [default to 4]
**posts_per_week** | [**FreeToolPlanContentCalendarRequestPostsPerWeek**](FreeToolPlanContentCalendarRequestPostsPerWeek.md) |  | 
**times** | [**FreeToolPlanContentCalendarRequestTimes**](FreeToolPlanContentCalendarRequestTimes.md) |  | [optional] 
**pillars** | **List[str]** | Content themes, rotated over the posts in date order. | [optional] 

## Example

```python
from postboost.models.free_tool_plan_content_calendar_request import FreeToolPlanContentCalendarRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPlanContentCalendarRequest from a JSON string
free_tool_plan_content_calendar_request_instance = FreeToolPlanContentCalendarRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolPlanContentCalendarRequest.to_json())

# convert the object into a dict
free_tool_plan_content_calendar_request_dict = free_tool_plan_content_calendar_request_instance.to_dict()
# create an instance of FreeToolPlanContentCalendarRequest from a dict
free_tool_plan_content_calendar_request_from_dict = FreeToolPlanContentCalendarRequest.from_dict(free_tool_plan_content_calendar_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



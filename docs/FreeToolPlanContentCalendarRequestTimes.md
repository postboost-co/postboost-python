# FreeToolPlanContentCalendarRequestTimes

Posting time per network (HH:MM, local time). A second post on the same day (over 7 a week) goes 3 hours later, or 3 hours earlier if later passes midnight.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**instagram** | **str** |  | [optional] [default to '10:00']
**facebook** | **str** |  | [optional] [default to '10:00']
**linkedin** | **str** |  | [optional] [default to '10:00']
**x** | **str** |  | [optional] [default to '10:00']
**tiktok** | **str** |  | [optional] [default to '10:00']
**youtube** | **str** |  | [optional] [default to '10:00']
**pinterest** | **str** |  | [optional] [default to '10:00']
**threads** | **str** |  | [optional] [default to '10:00']
**bluesky** | **str** |  | [optional] [default to '10:00']
**mastodon** | **str** |  | [optional] [default to '10:00']
**gbp** | **str** |  | [optional] [default to '10:00']

## Example

```python
from postboost.models.free_tool_plan_content_calendar_request_times import FreeToolPlanContentCalendarRequestTimes

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPlanContentCalendarRequestTimes from a JSON string
free_tool_plan_content_calendar_request_times_instance = FreeToolPlanContentCalendarRequestTimes.from_json(json)
# print the JSON string representation of the object
print(FreeToolPlanContentCalendarRequestTimes.to_json())

# convert the object into a dict
free_tool_plan_content_calendar_request_times_dict = free_tool_plan_content_calendar_request_times_instance.to_dict()
# create an instance of FreeToolPlanContentCalendarRequestTimes from a dict
free_tool_plan_content_calendar_request_times_from_dict = FreeToolPlanContentCalendarRequestTimes.from_dict(free_tool_plan_content_calendar_request_times_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



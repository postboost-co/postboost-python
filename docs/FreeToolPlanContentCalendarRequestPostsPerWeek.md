# FreeToolPlanContentCalendarRequestPostsPerWeek

Posts per week for each network you plan for (0 or missing = none).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**instagram** | **int** |  | [optional] [default to 0]
**facebook** | **int** |  | [optional] [default to 0]
**linkedin** | **int** |  | [optional] [default to 0]
**x** | **int** |  | [optional] [default to 0]
**tiktok** | **int** |  | [optional] [default to 0]
**youtube** | **int** |  | [optional] [default to 0]
**pinterest** | **int** |  | [optional] [default to 0]
**threads** | **int** |  | [optional] [default to 0]
**bluesky** | **int** |  | [optional] [default to 0]
**mastodon** | **int** |  | [optional] [default to 0]
**gbp** | **int** |  | [optional] [default to 0]

## Example

```python
from postboost.models.free_tool_plan_content_calendar_request_posts_per_week import FreeToolPlanContentCalendarRequestPostsPerWeek

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPlanContentCalendarRequestPostsPerWeek from a JSON string
free_tool_plan_content_calendar_request_posts_per_week_instance = FreeToolPlanContentCalendarRequestPostsPerWeek.from_json(json)
# print the JSON string representation of the object
print(FreeToolPlanContentCalendarRequestPostsPerWeek.to_json())

# convert the object into a dict
free_tool_plan_content_calendar_request_posts_per_week_dict = free_tool_plan_content_calendar_request_posts_per_week_instance.to_dict()
# create an instance of FreeToolPlanContentCalendarRequestPostsPerWeek from a dict
free_tool_plan_content_calendar_request_posts_per_week_from_dict = FreeToolPlanContentCalendarRequestPostsPerWeek.from_dict(free_tool_plan_content_calendar_request_posts_per_week_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



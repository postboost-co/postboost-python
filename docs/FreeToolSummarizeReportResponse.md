# FreeToolSummarizeReportResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**posts** | **int** |  | [optional] 
**date_range** | [**FreeToolSummarizeReportResponseDateRange**](FreeToolSummarizeReportResponseDateRange.md) |  | [optional] 
**views** | **int** |  | [optional] 
**engagements** | **int** |  | [optional] 
**engagement_rate** | **float** | Percent, 2 decimals; null without views. | [optional] 
**engagements_from** | **List[str]** | The counts added up as engagements. | [optional] 
**networks** | [**List[FreeToolSummarizeReportResponseNetworksInner]**](FreeToolSummarizeReportResponseNetworksInner.md) |  | [optional] 
**top_posts** | [**List[FreeToolSummarizeReportResponseTopPostsInner]**](FreeToolSummarizeReportResponseTopPostsInner.md) |  | [optional] 
**weekdays** | [**List[FreeToolSummarizeReportResponseWeekdaysInner]**](FreeToolSummarizeReportResponseWeekdaysInner.md) |  | [optional] 
**best_weekday** | **str** | The weekday with the highest average engagements per post. | [optional] 

## Example

```python
from postboost.models.free_tool_summarize_report_response import FreeToolSummarizeReportResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolSummarizeReportResponse from a JSON string
free_tool_summarize_report_response_instance = FreeToolSummarizeReportResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolSummarizeReportResponse.to_json())

# convert the object into a dict
free_tool_summarize_report_response_dict = free_tool_summarize_report_response_instance.to_dict()
# create an instance of FreeToolSummarizeReportResponse from a dict
free_tool_summarize_report_response_from_dict = FreeToolSummarizeReportResponse.from_dict(free_tool_summarize_report_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



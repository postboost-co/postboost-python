# FreeToolSummarizeReportRequestRowsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **str** | Publish date; only a leading YYYY-MM-DD is read. | [optional] 
**network** | **str** |  | [optional] 
**text** | **str** | The post text, a full caption is fine; the top posts show its first 80 characters. | [optional] 
**views** | **int** |  | [optional] 
**likes** | **int** |  | [optional] 
**comments** | **int** |  | [optional] 
**shares** | **int** |  | [optional] 
**clicks** | **int** |  | [optional] 
**engagements** | **int** |  | [optional] 

## Example

```python
from postboost.models.free_tool_summarize_report_request_rows_inner import FreeToolSummarizeReportRequestRowsInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolSummarizeReportRequestRowsInner from a JSON string
free_tool_summarize_report_request_rows_inner_instance = FreeToolSummarizeReportRequestRowsInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolSummarizeReportRequestRowsInner.to_json())

# convert the object into a dict
free_tool_summarize_report_request_rows_inner_dict = free_tool_summarize_report_request_rows_inner_instance.to_dict()
# create an instance of FreeToolSummarizeReportRequestRowsInner from a dict
free_tool_summarize_report_request_rows_inner_from_dict = FreeToolSummarizeReportRequestRowsInner.from_dict(free_tool_summarize_report_request_rows_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



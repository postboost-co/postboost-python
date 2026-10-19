# FreeToolSummarizeReportRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rows** | [**List[FreeToolSummarizeReportRequestRowsInner]**](FreeToolSummarizeReportRequestRowsInner.md) | One object per post, already mapped to these fields. Leave out a count the export does not have. | 

## Example

```python
from postboost.models.free_tool_summarize_report_request import FreeToolSummarizeReportRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolSummarizeReportRequest from a JSON string
free_tool_summarize_report_request_instance = FreeToolSummarizeReportRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolSummarizeReportRequest.to_json())

# convert the object into a dict
free_tool_summarize_report_request_dict = free_tool_summarize_report_request_instance.to_dict()
# create an instance of FreeToolSummarizeReportRequest from a dict
free_tool_summarize_report_request_from_dict = FreeToolSummarizeReportRequest.from_dict(free_tool_summarize_report_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



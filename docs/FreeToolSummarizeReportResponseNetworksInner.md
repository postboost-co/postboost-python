# FreeToolSummarizeReportResponseNetworksInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**network** | **str** |  | [optional] 
**posts** | **int** |  | [optional] 
**views** | **int** |  | [optional] 
**engagements** | **int** |  | [optional] 
**rate** | **float** | Percent, 2 decimals; null without views. | [optional] 

## Example

```python
from postboost.models.free_tool_summarize_report_response_networks_inner import FreeToolSummarizeReportResponseNetworksInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolSummarizeReportResponseNetworksInner from a JSON string
free_tool_summarize_report_response_networks_inner_instance = FreeToolSummarizeReportResponseNetworksInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolSummarizeReportResponseNetworksInner.to_json())

# convert the object into a dict
free_tool_summarize_report_response_networks_inner_dict = free_tool_summarize_report_response_networks_inner_instance.to_dict()
# create an instance of FreeToolSummarizeReportResponseNetworksInner from a dict
free_tool_summarize_report_response_networks_inner_from_dict = FreeToolSummarizeReportResponseNetworksInner.from_dict(free_tool_summarize_report_response_networks_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



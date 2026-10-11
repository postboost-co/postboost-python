# AnalyticsSummary


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | [**AnalyticsPeriod**](AnalyticsPeriod.md) |  | 
**data** | [**AnalyticsSummaryData**](AnalyticsSummaryData.md) |  | 

## Example

```python
from postboost.models.analytics_summary import AnalyticsSummary

# TODO update the JSON string below
json = "{}"
# create an instance of AnalyticsSummary from a JSON string
analytics_summary_instance = AnalyticsSummary.from_json(json)
# print the JSON string representation of the object
print(AnalyticsSummary.to_json())

# convert the object into a dict
analytics_summary_dict = analytics_summary_instance.to_dict()
# create an instance of AnalyticsSummary from a dict
analytics_summary_from_dict = AnalyticsSummary.from_dict(analytics_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



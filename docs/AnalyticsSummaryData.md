# AnalyticsSummaryData

Cross-platform summary over every account that supports analytics. Chart series are lists of `{date, value}` points (or `{label, value}` when the axis is not a date). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total_followers** | **int** |  | [optional] 
**follower_growth** | **Dict[str, object]** | Growth in the period with the change against the previous period. | [optional] 
**total_posts** | **Dict[str, object]** | Posts in the period with the change against the previous period. | [optional] 
**best_account** | **Dict[str, object]** |  | [optional] 
**needs_attention** | **Dict[str, object]** |  | [optional] 
**audience_chart** | **List[Dict[str, object]]** |  | [optional] 
**leaderboard** | **List[Dict[str, object]]** |  | [optional] 
**most_active** | **Dict[str, object]** |  | [optional] 
**least_active** | **Dict[str, object]** |  | [optional] 
**follower_distribution** | **List[Dict[str, object]]** |  | [optional] 
**posting_streak** | **Dict[str, object]** |  | [optional] 

## Example

```python
from postboost.models.analytics_summary_data import AnalyticsSummaryData

# TODO update the JSON string below
json = "{}"
# create an instance of AnalyticsSummaryData from a JSON string
analytics_summary_data_instance = AnalyticsSummaryData.from_json(json)
# print the JSON string representation of the object
print(AnalyticsSummaryData.to_json())

# convert the object into a dict
analytics_summary_data_dict = analytics_summary_data_instance.to_dict()
# create an instance of AnalyticsSummaryData from a dict
analytics_summary_data_from_dict = AnalyticsSummaryData.from_dict(analytics_summary_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



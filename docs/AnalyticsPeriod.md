# AnalyticsPeriod


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**start_date** | **date** |  | 
**end_date** | **date** |  | 
**previous_start_date** | **date** | Start of the equally long range before this one, used for comparisons. | 
**previous_end_date** | **date** |  | 

## Example

```python
from postboost.models.analytics_period import AnalyticsPeriod

# TODO update the JSON string below
json = "{}"
# create an instance of AnalyticsPeriod from a JSON string
analytics_period_instance = AnalyticsPeriod.from_json(json)
# print the JSON string representation of the object
print(AnalyticsPeriod.to_json())

# convert the object into a dict
analytics_period_dict = analytics_period_instance.to_dict()
# create an instance of AnalyticsPeriod from a dict
analytics_period_from_dict = AnalyticsPeriod.from_dict(analytics_period_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



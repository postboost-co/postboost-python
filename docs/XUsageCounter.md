# XUsageCounter


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**used** | **int** |  | 
**limit** | **int** | Monthly allowance; null &#x3D; unlimited. | 

## Example

```python
from postboost.models.x_usage_counter import XUsageCounter

# TODO update the JSON string below
json = "{}"
# create an instance of XUsageCounter from a JSON string
x_usage_counter_instance = XUsageCounter.from_json(json)
# print the JSON string representation of the object
print(XUsageCounter.to_json())

# convert the object into a dict
x_usage_counter_dict = x_usage_counter_instance.to_dict()
# create an instance of XUsageCounter from a dict
x_usage_counter_from_dict = XUsageCounter.from_dict(x_usage_counter_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



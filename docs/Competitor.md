# Competitor


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**account_id** | **int** |  | 
**username** | **str** |  | 
**name** | **str** |  | [optional] 
**image** | **str** |  | [optional] 
**followers_count** | **int** |  | [optional] 
**media_count** | **int** |  | [optional] 
**avg_engagement** | **int** | Average likes plus comments per imported post. | 
**last_snapshot_date** | **date** |  | [optional] 

## Example

```python
from postboost.models.competitor import Competitor

# TODO update the JSON string below
json = "{}"
# create an instance of Competitor from a JSON string
competitor_instance = Competitor.from_json(json)
# print the JSON string representation of the object
print(Competitor.to_json())

# convert the object into a dict
competitor_dict = competitor_instance.to_dict()
# create an instance of Competitor from a dict
competitor_from_dict = Competitor.from_dict(competitor_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



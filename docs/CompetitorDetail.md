# CompetitorDetail


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
**snapshots** | [**List[CompetitorSnapshot]**](CompetitorSnapshot.md) |  | 
**recent_media** | [**List[CompetitorMedia]**](CompetitorMedia.md) |  | 

## Example

```python
from postboost.models.competitor_detail import CompetitorDetail

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorDetail from a JSON string
competitor_detail_instance = CompetitorDetail.from_json(json)
# print the JSON string representation of the object
print(CompetitorDetail.to_json())

# convert the object into a dict
competitor_detail_dict = competitor_detail_instance.to_dict()
# create an instance of CompetitorDetail from a dict
competitor_detail_from_dict = CompetitorDetail.from_dict(competitor_detail_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



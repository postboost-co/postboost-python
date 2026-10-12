# CompetitorSnapshot


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **date** |  | [optional] 
**followers_count** | **int** |  | [optional] 
**media_count** | **int** |  | [optional] 

## Example

```python
from postboost.models.competitor_snapshot import CompetitorSnapshot

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorSnapshot from a JSON string
competitor_snapshot_instance = CompetitorSnapshot.from_json(json)
# print the JSON string representation of the object
print(CompetitorSnapshot.to_json())

# convert the object into a dict
competitor_snapshot_dict = competitor_snapshot_instance.to_dict()
# create an instance of CompetitorSnapshot from a dict
competitor_snapshot_from_dict = CompetitorSnapshot.from_dict(competitor_snapshot_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



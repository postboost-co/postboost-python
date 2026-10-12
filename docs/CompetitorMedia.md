# CompetitorMedia


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**caption** | **str** |  | [optional] 
**permalink** | **str** |  | [optional] 
**media_type** | **str** |  | [optional] 
**like_count** | **int** |  | [optional] 
**comments_count** | **int** |  | [optional] 
**timestamp** | **datetime** |  | [optional] 

## Example

```python
from postboost.models.competitor_media import CompetitorMedia

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorMedia from a JSON string
competitor_media_instance = CompetitorMedia.from_json(json)
# print the JSON string representation of the object
print(CompetitorMedia.to_json())

# convert the object into a dict
competitor_media_dict = competitor_media_instance.to_dict()
# create an instance of CompetitorMedia from a dict
competitor_media_from_dict = CompetitorMedia.from_dict(competitor_media_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



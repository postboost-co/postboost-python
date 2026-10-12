# RssFeedUpdate


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**account_ids** | **List[int]** |  | [optional] 
**mode** | **str** |  | [optional] 
**template** | **str** |  | [optional] 
**max_items_per_run** | **int** |  | [optional] 
**active** | **bool** |  | [optional] 

## Example

```python
from postboost.models.rss_feed_update import RssFeedUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of RssFeedUpdate from a JSON string
rss_feed_update_instance = RssFeedUpdate.from_json(json)
# print the JSON string representation of the object
print(RssFeedUpdate.to_json())

# convert the object into a dict
rss_feed_update_dict = rss_feed_update_instance.to_dict()
# create an instance of RssFeedUpdate from a dict
rss_feed_update_from_dict = RssFeedUpdate.from_dict(rss_feed_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



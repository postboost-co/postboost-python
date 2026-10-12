# RssFeed


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** |  | 
**url** | **str** |  | 
**name** | **str** |  | 
**account_ids** | **List[int]** |  | 
**mode** | **str** |  | 
**template** | **str** |  | 
**max_items_per_run** | **int** |  | 
**active** | **bool** |  | 
**last_polled_at** | **datetime** |  | 
**last_error** | **str** | Error of the last check; after 5 failures in a row the feed is checked every 6 hours. | 
**created_at** | **datetime** |  | 

## Example

```python
from postboost.models.rss_feed import RssFeed

# TODO update the JSON string below
json = "{}"
# create an instance of RssFeed from a JSON string
rss_feed_instance = RssFeed.from_json(json)
# print the JSON string representation of the object
print(RssFeed.to_json())

# convert the object into a dict
rss_feed_dict = rss_feed_instance.to_dict()
# create an instance of RssFeed from a dict
rss_feed_from_dict = RssFeed.from_dict(rss_feed_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



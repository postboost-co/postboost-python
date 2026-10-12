# ListRssFeeds200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[RssFeed]**](RssFeed.md) |  | 

## Example

```python
from postboost.models.list_rss_feeds200_response import ListRssFeeds200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListRssFeeds200Response from a JSON string
list_rss_feeds200_response_instance = ListRssFeeds200Response.from_json(json)
# print the JSON string representation of the object
print(ListRssFeeds200Response.to_json())

# convert the object into a dict
list_rss_feeds200_response_dict = list_rss_feeds200_response_instance.to_dict()
# create an instance of ListRssFeeds200Response from a dict
list_rss_feeds200_response_from_dict = ListRssFeeds200Response.from_dict(list_rss_feeds200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



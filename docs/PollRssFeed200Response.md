# PollRssFeed200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**created** | **int** | Posts created from new items. | 
**skipped** | **int** | New items refused by a guardrail. | 
**data** | [**RssFeed**](RssFeed.md) |  | 

## Example

```python
from postboost.models.poll_rss_feed200_response import PollRssFeed200Response

# TODO update the JSON string below
json = "{}"
# create an instance of PollRssFeed200Response from a JSON string
poll_rss_feed200_response_instance = PollRssFeed200Response.from_json(json)
# print the JSON string representation of the object
print(PollRssFeed200Response.to_json())

# convert the object into a dict
poll_rss_feed200_response_dict = poll_rss_feed200_response_instance.to_dict()
# create an instance of PollRssFeed200Response from a dict
poll_rss_feed200_response_from_dict = PollRssFeed200Response.from_dict(poll_rss_feed200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# RssFeedInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** | Public http(s) URL of an RSS 2.0 or Atom feed. | 
**name** | **str** |  | [optional] 
**account_ids** | **List[int]** |  | 
**mode** | **str** |  | [optional] [default to 'draft']
**template** | **str** | Post text. Placeholders: &#x60;{title}&#x60;, &#x60;{link}&#x60;, &#x60;{summary}&#x60; (up to 280 characters). Default &#x60;{title}&#x60; + blank line + &#x60;{link}&#x60;. | [optional] 
**max_items_per_run** | **int** |  | [optional] [default to 3]
**active** | **bool** |  | [optional] [default to True]

## Example

```python
from postboost.models.rss_feed_input import RssFeedInput

# TODO update the JSON string below
json = "{}"
# create an instance of RssFeedInput from a JSON string
rss_feed_input_instance = RssFeedInput.from_json(json)
# print the JSON string representation of the object
print(RssFeedInput.to_json())

# convert the object into a dict
rss_feed_input_dict = rss_feed_input_instance.to_dict()
# create an instance of RssFeedInput from a dict
rss_feed_input_from_dict = RssFeedInput.from_dict(rss_feed_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



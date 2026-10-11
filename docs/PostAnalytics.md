# PostAnalytics


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**summary** | **Dict[str, object]** | Totals (views, likes, comments, shares), trends, engagement rate, breakdown, funnel and peak day across the post&#39;s accounts. Empty when nothing is published yet. | 
**winner** | **object** |  | [optional] 
**accounts** | **List[Dict[str, object]]** |  | 

## Example

```python
from postboost.models.post_analytics import PostAnalytics

# TODO update the JSON string below
json = "{}"
# create an instance of PostAnalytics from a JSON string
post_analytics_instance = PostAnalytics.from_json(json)
# print the JSON string representation of the object
print(PostAnalytics.to_json())

# convert the object into a dict
post_analytics_dict = post_analytics_instance.to_dict()
# create an instance of PostAnalytics from a dict
post_analytics_from_dict = PostAnalytics.from_dict(post_analytics_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



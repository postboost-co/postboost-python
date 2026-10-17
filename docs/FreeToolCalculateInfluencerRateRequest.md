# FreeToolCalculateInfluencerRateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**network** | **str** | LinkedIn is not offered: no primary source for its rates. | 
**followers** | **int** | Followers (subscribers on YouTube). Sets the tier. | 
**deliverable** | **str** | Instagram: post (default), reel, carousel. TikTok: video. X and Facebook: post. YouTube: integration (default), dedicated, short. | [optional] 
**avg_views** | **int** | Expected views of the deliverable. Required on YouTube, which is priced per 1,000 views; with cpm_usd it gives your own CPM estimate on any network. | [optional] 
**cpm_usd** | **int** | Your own price per 1,000 views, in whole USD, for the CPM estimate. | [optional] 
**usage_rights_months** | **int** | Months the brand may reuse the content. | [optional] [default to 0]
**exclusivity** | **bool** | The creator agrees not to work with competitors for the campaign. | [optional] [default to False]

## Example

```python
from postboost.models.free_tool_calculate_influencer_rate_request import FreeToolCalculateInfluencerRateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateInfluencerRateRequest from a JSON string
free_tool_calculate_influencer_rate_request_instance = FreeToolCalculateInfluencerRateRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateInfluencerRateRequest.to_json())

# convert the object into a dict
free_tool_calculate_influencer_rate_request_dict = free_tool_calculate_influencer_rate_request_instance.to_dict()
# create an instance of FreeToolCalculateInfluencerRateRequest from a dict
free_tool_calculate_influencer_rate_request_from_dict = FreeToolCalculateInfluencerRateRequest.from_dict(free_tool_calculate_influencer_rate_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



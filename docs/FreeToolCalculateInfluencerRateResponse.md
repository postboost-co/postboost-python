# FreeToolCalculateInfluencerRateResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tier** | **str** |  | [optional] 
**tier_label** | **str** |  | [optional] 
**deliverable** | **str** |  | [optional] 
**guide_low** | **int** | USD, low end of the vendor price-guide range after the adjustments. | [optional] 
**guide_high** | **int** | USD, high end; null when the guide is open-ended (e.g. 10,000+). | [optional] 
**guide_source** | [**FreeToolCalculateInfluencerRateResponseGuideSource**](FreeToolCalculateInfluencerRateResponseGuideSource.md) |  | [optional] 
**marketplace_median** | **int** | USD, the measured median paid deliverable for this tier, all networks, before adjustments. | [optional] 
**marketplace_note** | **str** |  | [optional] 
**marketplace_source** | [**FreeToolCalculateInfluencerRateResponseGuideSource**](FreeToolCalculateInfluencerRateResponseGuideSource.md) |  | [optional] 
**cpm_estimate** | **int** | USD, avg_views / 1,000 × cpm_usd (half up); null without both. | [optional] 
**multipliers** | [**List[FreeToolCalculateInfluencerRateResponseMultipliersInner]**](FreeToolCalculateInfluencerRateResponseMultipliersInner.md) | Every adjustment applied, as a percent of the base price. | [optional] 
**method** | **str** |  | [optional] 
**warnings** | **List[str]** |  | [optional] 
**currency** | **str** |  | [optional] 
**last_verified** | **date** |  | [optional] 

## Example

```python
from postboost.models.free_tool_calculate_influencer_rate_response import FreeToolCalculateInfluencerRateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCalculateInfluencerRateResponse from a JSON string
free_tool_calculate_influencer_rate_response_instance = FreeToolCalculateInfluencerRateResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCalculateInfluencerRateResponse.to_json())

# convert the object into a dict
free_tool_calculate_influencer_rate_response_dict = free_tool_calculate_influencer_rate_response_instance.to_dict()
# create an instance of FreeToolCalculateInfluencerRateResponse from a dict
free_tool_calculate_influencer_rate_response_from_dict = FreeToolCalculateInfluencerRateResponse.from_dict(free_tool_calculate_influencer_rate_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



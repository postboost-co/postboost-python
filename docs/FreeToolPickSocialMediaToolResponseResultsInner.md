# FreeToolPickSocialMediaToolResponseResultsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slug** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**score** | **int** | How many of your needs the tool meets. | [optional] 
**matched** | **List[str]** |  | [optional] 
**missing** | **List[str]** |  | [optional] 
**unknown** | **List[str]** | Needs the tool&#39;s public docs did not show either way (\&quot;not documented\&quot;). | [optional] 
**compare_url** | **str** | Path of the full PostBoost comparison page; null for PostBoost. | [optional] 
**checked_at** | **date** | When the tool&#39;s data was last checked. | [optional] 
**pick_if** | **str** | When this tool is the better choice; null for PostBoost. | [optional] 
**postboost_if** | **str** | When PostBoost is the better choice; null for PostBoost. | [optional] 

## Example

```python
from postboost.models.free_tool_pick_social_media_tool_response_results_inner import FreeToolPickSocialMediaToolResponseResultsInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPickSocialMediaToolResponseResultsInner from a JSON string
free_tool_pick_social_media_tool_response_results_inner_instance = FreeToolPickSocialMediaToolResponseResultsInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolPickSocialMediaToolResponseResultsInner.to_json())

# convert the object into a dict
free_tool_pick_social_media_tool_response_results_inner_dict = free_tool_pick_social_media_tool_response_results_inner_instance.to_dict()
# create an instance of FreeToolPickSocialMediaToolResponseResultsInner from a dict
free_tool_pick_social_media_tool_response_results_inner_from_dict = FreeToolPickSocialMediaToolResponseResultsInner.from_dict(free_tool_pick_social_media_tool_response_results_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



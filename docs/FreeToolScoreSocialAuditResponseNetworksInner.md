# FreeToolScoreSocialAuditResponseNetworksInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**network** | **str** |  | [optional] 
**label** | **str** |  | [optional] 
**score** | **int** |  | [optional] 
**points** | **int** |  | [optional] 
**max_points** | **int** |  | [optional] 
**items** | [**List[FreeToolScoreSocialAuditResponseNetworksInnerItemsInner]**](FreeToolScoreSocialAuditResponseNetworksInnerItemsInner.md) |  | [optional] 

## Example

```python
from postboost.models.free_tool_score_social_audit_response_networks_inner import FreeToolScoreSocialAuditResponseNetworksInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolScoreSocialAuditResponseNetworksInner from a JSON string
free_tool_score_social_audit_response_networks_inner_instance = FreeToolScoreSocialAuditResponseNetworksInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolScoreSocialAuditResponseNetworksInner.to_json())

# convert the object into a dict
free_tool_score_social_audit_response_networks_inner_dict = free_tool_score_social_audit_response_networks_inner_instance.to_dict()
# create an instance of FreeToolScoreSocialAuditResponseNetworksInner from a dict
free_tool_score_social_audit_response_networks_inner_from_dict = FreeToolScoreSocialAuditResponseNetworksInner.from_dict(free_tool_score_social_audit_response_networks_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



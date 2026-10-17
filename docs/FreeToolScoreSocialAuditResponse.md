# FreeToolScoreSocialAuditResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**score** | **int** | Overall score: all points over the maximum, as 0-100 rounded half up. | [optional] 
**networks** | [**List[FreeToolScoreSocialAuditResponseNetworksInner]**](FreeToolScoreSocialAuditResponseNetworksInner.md) | One row per audited network, in a fixed network order. | [optional] 
**top_fixes** | [**List[FreeToolScoreSocialAuditResponseTopFixesInner]**](FreeToolScoreSocialAuditResponseTopFixesInner.md) | Up to 3 questions with the fewest points over all audited networks (ties: checklist order); only questions answered below yes somewhere. | [optional] 
**report_markdown** | **str** | The scorecard as a Markdown report: overall score, top fixes and every answer per network. | [optional] 

## Example

```python
from postboost.models.free_tool_score_social_audit_response import FreeToolScoreSocialAuditResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolScoreSocialAuditResponse from a JSON string
free_tool_score_social_audit_response_instance = FreeToolScoreSocialAuditResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolScoreSocialAuditResponse.to_json())

# convert the object into a dict
free_tool_score_social_audit_response_dict = free_tool_score_social_audit_response_instance.to_dict()
# create an instance of FreeToolScoreSocialAuditResponse from a dict
free_tool_score_social_audit_response_from_dict = FreeToolScoreSocialAuditResponse.from_dict(free_tool_score_social_audit_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



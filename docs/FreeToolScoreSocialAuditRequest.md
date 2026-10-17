# FreeToolScoreSocialAuditRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**target_posts_per_week** | **int** | Your own posting target per network and week, used in the frequency question. | [optional] [default to 3]
**instagram** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] 
**facebook** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] 
**linkedin** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] 
**x** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] 
**tiktok** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] 
**youtube** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] 
**pinterest** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] 
**threads** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] 
**bluesky** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] 
**mastodon** | [**FreeToolScoreSocialAuditRequestInstagram**](FreeToolScoreSocialAuditRequestInstagram.md) |  | [optional] 

## Example

```python
from postboost.models.free_tool_score_social_audit_request import FreeToolScoreSocialAuditRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolScoreSocialAuditRequest from a JSON string
free_tool_score_social_audit_request_instance = FreeToolScoreSocialAuditRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolScoreSocialAuditRequest.to_json())

# convert the object into a dict
free_tool_score_social_audit_request_dict = free_tool_score_social_audit_request_instance.to_dict()
# create an instance of FreeToolScoreSocialAuditRequest from a dict
free_tool_score_social_audit_request_from_dict = FreeToolScoreSocialAuditRequest.from_dict(free_tool_score_social_audit_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



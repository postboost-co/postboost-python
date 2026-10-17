# FreeToolScoreSocialAuditRequestInstagram

Your answers for this network: yes, partly or no per question (a missing answer counts as no). Leave the network out to skip it.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile** | **str** | Profile photo, name and cover image match your brand. | [optional] [default to 'no']
**bio** | **str** | Your bio says who you help and how, and has a link. | [optional] [default to 'no']
**link_tracking** | **str** | The bio link carries UTM tags. | [optional] [default to 'no']
**frequency** | **str** | You publish at least N posts a week, your own target. | [optional] [default to 'no']
**replies** | **str** | You reply to comments and messages within 24 hours. | [optional] [default to 'no']
**native_formats** | **str** | You use the formats the network is built for, such as short video, carousels or documents. | [optional] [default to 'no']
**pinned** | **str** | Your pinned or featured post is current. | [optional] [default to 'no']
**engagement_rate** | **str** | You check your engagement rate every month. | [optional] [default to 'no']

## Example

```python
from postboost.models.free_tool_score_social_audit_request_instagram import FreeToolScoreSocialAuditRequestInstagram

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolScoreSocialAuditRequestInstagram from a JSON string
free_tool_score_social_audit_request_instagram_instance = FreeToolScoreSocialAuditRequestInstagram.from_json(json)
# print the JSON string representation of the object
print(FreeToolScoreSocialAuditRequestInstagram.to_json())

# convert the object into a dict
free_tool_score_social_audit_request_instagram_dict = free_tool_score_social_audit_request_instagram_instance.to_dict()
# create an instance of FreeToolScoreSocialAuditRequestInstagram from a dict
free_tool_score_social_audit_request_instagram_from_dict = FreeToolScoreSocialAuditRequestInstagram.from_dict(free_tool_score_social_audit_request_instagram_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



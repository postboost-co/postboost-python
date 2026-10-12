# ApproveAgentProposal409Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**data** | [**AgentProposal**](AgentProposal.md) |  | 

## Example

```python
from postboost.models.approve_agent_proposal409_response import ApproveAgentProposal409Response

# TODO update the JSON string below
json = "{}"
# create an instance of ApproveAgentProposal409Response from a JSON string
approve_agent_proposal409_response_instance = ApproveAgentProposal409Response.from_json(json)
# print the JSON string representation of the object
print(ApproveAgentProposal409Response.to_json())

# convert the object into a dict
approve_agent_proposal409_response_dict = approve_agent_proposal409_response_instance.to_dict()
# create an instance of ApproveAgentProposal409Response from a dict
approve_agent_proposal409_response_from_dict = ApproveAgentProposal409Response.from_dict(approve_agent_proposal409_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



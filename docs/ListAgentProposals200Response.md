# ListAgentProposals200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[AgentProposal]**](AgentProposal.md) |  | 
**meta** | [**AgentPageMeta**](AgentPageMeta.md) |  | 

## Example

```python
from postboost.models.list_agent_proposals200_response import ListAgentProposals200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListAgentProposals200Response from a JSON string
list_agent_proposals200_response_instance = ListAgentProposals200Response.from_json(json)
# print the JSON string representation of the object
print(ListAgentProposals200Response.to_json())

# convert the object into a dict
list_agent_proposals200_response_dict = list_agent_proposals200_response_instance.to_dict()
# create an instance of ListAgentProposals200Response from a dict
list_agent_proposals200_response_from_dict = ListAgentProposals200Response.from_dict(list_agent_proposals200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# ListAgentRuns200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**List[AgentRun]**](AgentRun.md) |  | 
**meta** | [**AgentPageMeta**](AgentPageMeta.md) |  | 

## Example

```python
from postboost.models.list_agent_runs200_response import ListAgentRuns200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListAgentRuns200Response from a JSON string
list_agent_runs200_response_instance = ListAgentRuns200Response.from_json(json)
# print the JSON string representation of the object
print(ListAgentRuns200Response.to_json())

# convert the object into a dict
list_agent_runs200_response_dict = list_agent_runs200_response_instance.to_dict()
# create an instance of ListAgentRuns200Response from a dict
list_agent_runs200_response_from_dict = ListAgentRuns200Response.from_dict(list_agent_runs200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# AgentRun


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** |  | 
**agent_uuid** | **str** |  | 
**agent_type** | **str** |  | 
**trigger** | **str** |  | 
**status** | **str** |  | 
**started_at** | **datetime** |  | [optional] 
**finished_at** | **datetime** |  | [optional] 
**items_checked** | **int** |  | 
**proposals_created** | **int** |  | 
**credits_used** | **int** | AI credits this run used. | 
**summary** | **str** |  | [optional] 
**error** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**proposals** | [**List[AgentProposal]**](AgentProposal.md) | Only on &#x60;GET /agent-runs/{runUuid}&#x60;. | [optional] 

## Example

```python
from postboost.models.agent_run import AgentRun

# TODO update the JSON string below
json = "{}"
# create an instance of AgentRun from a JSON string
agent_run_instance = AgentRun.from_json(json)
# print the JSON string representation of the object
print(AgentRun.to_json())

# convert the object into a dict
agent_run_dict = agent_run_instance.to_dict()
# create an instance of AgentRun from a dict
agent_run_from_dict = AgentRun.from_dict(agent_run_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# AgentProposal


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** |  | 
**run_uuid** | **str** |  | [optional] 
**post_uuid** | **str** |  | [optional] 
**account_id** | **int** |  | [optional] 
**kind** | **str** | &#x60;hold_post&#x60; moves the post back to draft; &#x60;edit_caption&#x60; replaces one caption; &#x60;retry_account&#x60; publishes one failed account again; &#x60;reconnect_account&#x60; asks to reconnect the account first.  | 
**severity** | **str** |  | 
**reason** | **str** |  | 
**payload** | **Dict[str, object]** | The proposed change. &#x60;hold_post&#x60;: &#x60;reasons[]&#x60; (&#x60;code&#x60;, &#x60;account_id&#x60;, &#x60;message&#x60;, &#x60;severity&#x60;) and &#x60;scheduled_at&#x60;. &#x60;edit_caption&#x60;: &#x60;version_account_id&#x60; (0 &#x3D; original), &#x60;item_index&#x60;, &#x60;before&#x60;, &#x60;after&#x60;. &#x60;retry_account&#x60;: &#x60;error&#x60; (up to 300 characters) and, for a shortened caption, &#x60;source_account_id&#x60; (the version it was taken from, 0 &#x3D; original), &#x60;item_index&#x60;, &#x60;before&#x60;, &#x60;after&#x60;. &#x60;reconnect_account&#x60;: &#x60;error&#x60;, &#x60;reconnect_url&#x60;. All carry &#x60;post_updated_at&#x60;.  | 
**status** | **str** |  | 
**decided_at** | **datetime** |  | [optional] 
**applied_at** | **datetime** |  | [optional] 
**note** | **str** |  | [optional] 
**error** | **str** | Why a proposal went stale or failed. | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from postboost.models.agent_proposal import AgentProposal

# TODO update the JSON string below
json = "{}"
# create an instance of AgentProposal from a JSON string
agent_proposal_instance = AgentProposal.from_json(json)
# print the JSON string representation of the object
print(AgentProposal.to_json())

# convert the object into a dict
agent_proposal_dict = agent_proposal_instance.to_dict()
# create an instance of AgentProposal from a dict
agent_proposal_from_dict = AgentProposal.from_dict(agent_proposal_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



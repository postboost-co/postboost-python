# AgentPageMeta


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current_page** | **int** |  | 
**last_page** | **int** |  | 
**per_page** | **int** |  | 
**total** | **int** |  | 

## Example

```python
from postboost.models.agent_page_meta import AgentPageMeta

# TODO update the JSON string below
json = "{}"
# create an instance of AgentPageMeta from a JSON string
agent_page_meta_instance = AgentPageMeta.from_json(json)
# print the JSON string representation of the object
print(AgentPageMeta.to_json())

# convert the object into a dict
agent_page_meta_dict = agent_page_meta_instance.to_dict()
# create an instance of AgentPageMeta from a dict
agent_page_meta_from_dict = AgentPageMeta.from_dict(agent_page_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



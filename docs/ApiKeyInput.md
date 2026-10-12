# ApiKeyInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**abilities** | [**List[ApiKeyAbility]**](ApiKeyAbility.md) |  | 
**account_ids** | **List[int]** | Limit the key to these account ids of the workspace. Omit or null for every account. A limited key must send &#x60;account_ids&#x60; on recycling rules, report exports and AI drafts, and its lists show only its accounts. | [optional] 
**expires_at** | **date** | Last day the key works. Must be after today. Omit for no expiry. | [optional] 

## Example

```python
from postboost.models.api_key_input import ApiKeyInput

# TODO update the JSON string below
json = "{}"
# create an instance of ApiKeyInput from a JSON string
api_key_input_instance = ApiKeyInput.from_json(json)
# print the JSON string representation of the object
print(ApiKeyInput.to_json())

# convert the object into a dict
api_key_input_dict = api_key_input_instance.to_dict()
# create an instance of ApiKeyInput from a dict
api_key_input_from_dict = ApiKeyInput.from_dict(api_key_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



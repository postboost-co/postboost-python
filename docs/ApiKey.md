# ApiKey


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 
**abilities** | [**List[ApiKeyAbility]**](ApiKeyAbility.md) |  | 
**account_ids** | **List[int]** |  | [optional] 
**created_by** | **str** | Name of the user the key acts as. | [optional] 
**last_used_at** | **datetime** |  | [optional] 
**expires_at** | **date** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from postboost.models.api_key import ApiKey

# TODO update the JSON string below
json = "{}"
# create an instance of ApiKey from a JSON string
api_key_instance = ApiKey.from_json(json)
# print the JSON string representation of the object
print(ApiKey.to_json())

# convert the object into a dict
api_key_dict = api_key_instance.to_dict()
# create an instance of ApiKey from a dict
api_key_from_dict = ApiKey.from_dict(api_key_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



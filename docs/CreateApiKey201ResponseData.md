# CreateApiKey201ResponseData


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
**token** | **str** | The plain API key. Shown only in this response. | 

## Example

```python
from postboost.models.create_api_key201_response_data import CreateApiKey201ResponseData

# TODO update the JSON string below
json = "{}"
# create an instance of CreateApiKey201ResponseData from a JSON string
create_api_key201_response_data_instance = CreateApiKey201ResponseData.from_json(json)
# print the JSON string representation of the object
print(CreateApiKey201ResponseData.to_json())

# convert the object into a dict
create_api_key201_response_data_dict = create_api_key201_response_data_instance.to_dict()
# create an instance of CreateApiKey201ResponseData from a dict
create_api_key201_response_data_from_dict = CreateApiKey201ResponseData.from_dict(create_api_key201_response_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



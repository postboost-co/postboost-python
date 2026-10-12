# ApiActivity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**user_id** | **int** |  | [optional] 
**token_ref** | **str** | First 12 hex characters of the SHA-256 of the API token used, to tell tokens apart. | [optional] 
**client** | **str** | &#x60;X-PostBoost-Client&#x60; header, else the &#x60;User-Agent&#x60;. | [optional] 
**route_name** | **str** |  | [optional] 
**method** | **str** |  | 
**post_uuid** | **str** |  | [optional] 
**outcome** | [**ApiActivityOutcome**](ApiActivityOutcome.md) |  | 
**http_status** | **int** |  | 
**created_at** | **datetime** |  | 

## Example

```python
from postboost.models.api_activity import ApiActivity

# TODO update the JSON string below
json = "{}"
# create an instance of ApiActivity from a JSON string
api_activity_instance = ApiActivity.from_json(json)
# print the JSON string representation of the object
print(ApiActivity.to_json())

# convert the object into a dict
api_activity_dict = api_activity_instance.to_dict()
# create an instance of ApiActivity from a dict
api_activity_from_dict = ApiActivity.from_dict(api_activity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



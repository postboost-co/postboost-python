# GuardrailError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**code** | **str** |  | [optional] 
**account_id** | **int** | The account the problem is about. | [optional] 
**existing_post_uuid** | **str** | &#x60;duplicate_post&#x60; only: the earlier post with the same content. | [optional] 
**limit** | **int** | &#x60;account_daily_cap_reached&#x60; only: the account&#39;s daily cap. | [optional] 
**used** | **int** | &#x60;account_daily_cap_reached&#x60; only: posts already counted on that UTC day. | [optional] 

## Example

```python
from postboost.models.guardrail_error import GuardrailError

# TODO update the JSON string below
json = "{}"
# create an instance of GuardrailError from a JSON string
guardrail_error_instance = GuardrailError.from_json(json)
# print the JSON string representation of the object
print(GuardrailError.to_json())

# convert the object into a dict
guardrail_error_dict = guardrail_error_instance.to_dict()
# create an instance of GuardrailError from a dict
guardrail_error_from_dict = GuardrailError.from_dict(guardrail_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



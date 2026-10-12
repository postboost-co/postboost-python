# PreflightResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**valid** | **bool** | True when create-post with the same body would succeed. | 
**errors** | **Dict[str, List[str]]** | Validation and network-requirement errors keyed by field, as create-post would report them in a &#x60;422&#x60;. | 
**issues** | [**List[GuardrailError]**](GuardrailError.md) | Guardrail problems, in the order create-post would report the first of them. | 
**publish_at** | **datetime** | UTC time the post would publish at; null for a draft. | 
**accounts** | [**List[AccountHealth]**](AccountHealth.md) |  | 

## Example

```python
from postboost.models.preflight_result import PreflightResult

# TODO update the JSON string below
json = "{}"
# create an instance of PreflightResult from a JSON string
preflight_result_instance = PreflightResult.from_json(json)
# print the JSON string representation of the object
print(PreflightResult.to_json())

# convert the object into a dict
preflight_result_dict = preflight_result_instance.to_dict()
# create an instance of PreflightResult from a dict
preflight_result_from_dict = PreflightResult.from_dict(preflight_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



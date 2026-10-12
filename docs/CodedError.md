# CodedError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**code** | **str** | Machine-readable reason, e.g. &#x60;ai_credits_exhausted&#x60;, &#x60;image_credits_exhausted&#x60;, &#x60;not_enough_posts&#x60;. | [optional] 
**errors** | **Dict[str, object]** |  | [optional] 

## Example

```python
from postboost.models.coded_error import CodedError

# TODO update the JSON string below
json = "{}"
# create an instance of CodedError from a JSON string
coded_error_instance = CodedError.from_json(json)
# print the JSON string representation of the object
print(CodedError.to_json())

# convert the object into a dict
coded_error_dict = coded_error_instance.to_dict()
# create an instance of CodedError from a dict
coded_error_from_dict = CodedError.from_dict(coded_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



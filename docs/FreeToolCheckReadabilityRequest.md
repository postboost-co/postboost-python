# FreeToolCheckReadabilityRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | The post text. | 
**language** | **str** | Language code. Only English (&#x60;en&#x60;) is scored; other languages return &#x60;supported: false&#x60; and no scores. | [optional] [default to 'en']

## Example

```python
from postboost.models.free_tool_check_readability_request import FreeToolCheckReadabilityRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCheckReadabilityRequest from a JSON string
free_tool_check_readability_request_instance = FreeToolCheckReadabilityRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCheckReadabilityRequest.to_json())

# convert the object into a dict
free_tool_check_readability_request_dict = free_tool_check_readability_request_instance.to_dict()
# create an instance of FreeToolCheckReadabilityRequest from a dict
free_tool_check_readability_request_from_dict = FreeToolCheckReadabilityRequest.from_dict(free_tool_check_readability_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



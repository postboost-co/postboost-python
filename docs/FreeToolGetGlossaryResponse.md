# FreeToolGetGlossaryResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** | Number of terms returned. | [optional] 
**terms** | [**List[FreeToolGetGlossaryResponseTermsInner]**](FreeToolGetGlossaryResponseTermsInner.md) |  | [optional] 
**last_verified** | **date** | When the definitions were last checked against their sources. | [optional] 

## Example

```python
from postboost.models.free_tool_get_glossary_response import FreeToolGetGlossaryResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetGlossaryResponse from a JSON string
free_tool_get_glossary_response_instance = FreeToolGetGlossaryResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetGlossaryResponse.to_json())

# convert the object into a dict
free_tool_get_glossary_response_dict = free_tool_get_glossary_response_instance.to_dict()
# create an instance of FreeToolGetGlossaryResponse from a dict
free_tool_get_glossary_response_from_dict = FreeToolGetGlossaryResponse.from_dict(free_tool_get_glossary_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



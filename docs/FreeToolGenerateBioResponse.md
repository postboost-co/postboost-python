# FreeToolGenerateBioResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bios** | **List[str]** | Three to five different bios, each at most 150 characters as the character counter counts them (most emoji count as 2). | [optional] 
**credits_spent** | **int** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] 
**cached** | **bool** | True when the same request was answered before (free). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_bio_response import FreeToolGenerateBioResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateBioResponse from a JSON string
free_tool_generate_bio_response_instance = FreeToolGenerateBioResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateBioResponse.to_json())

# convert the object into a dict
free_tool_generate_bio_response_dict = free_tool_generate_bio_response_instance.to_dict()
# create an instance of FreeToolGenerateBioResponse from a dict
free_tool_generate_bio_response_from_dict = FreeToolGenerateBioResponse.from_dict(free_tool_generate_bio_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



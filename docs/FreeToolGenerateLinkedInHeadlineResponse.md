# FreeToolGenerateLinkedInHeadlineResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**headlines** | **List[str]** | Three to five different headlines, each at most 220 characters as the character counter counts them. | [optional] 
**credits_spent** | **int** | AI credits this call took from the workspace: 1, or 0 for a cached result. | [optional] 
**cached** | **bool** | True when the same request was answered before (free). | [optional] 

## Example

```python
from postboost.models.free_tool_generate_linked_in_headline_response import FreeToolGenerateLinkedInHeadlineResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateLinkedInHeadlineResponse from a JSON string
free_tool_generate_linked_in_headline_response_instance = FreeToolGenerateLinkedInHeadlineResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateLinkedInHeadlineResponse.to_json())

# convert the object into a dict
free_tool_generate_linked_in_headline_response_dict = free_tool_generate_linked_in_headline_response_instance.to_dict()
# create an instance of FreeToolGenerateLinkedInHeadlineResponse from a dict
free_tool_generate_linked_in_headline_response_from_dict = FreeToolGenerateLinkedInHeadlineResponse.from_dict(free_tool_generate_linked_in_headline_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



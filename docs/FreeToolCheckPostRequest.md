# FreeToolCheckPostRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** | The post text, up to 10,000 characters; 5,000 without an API token. | [optional] [default to '']
**networks** | **List[str]** | The networks to check the post for. | 
**media** | [**FreeToolCheckPostRequestMedia**](FreeToolCheckPostRequestMedia.md) |  | [optional] 

## Example

```python
from postboost.models.free_tool_check_post_request import FreeToolCheckPostRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCheckPostRequest from a JSON string
free_tool_check_post_request_instance = FreeToolCheckPostRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolCheckPostRequest.to_json())

# convert the object into a dict
free_tool_check_post_request_dict = free_tool_check_post_request_instance.to_dict()
# create an instance of FreeToolCheckPostRequest from a dict
free_tool_check_post_request_from_dict = FreeToolCheckPostRequest.from_dict(free_tool_check_post_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



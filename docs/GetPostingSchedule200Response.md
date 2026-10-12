# GetPostingSchedule200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**PostingSchedule**](PostingSchedule.md) |  | 

## Example

```python
from postboost.models.get_posting_schedule200_response import GetPostingSchedule200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetPostingSchedule200Response from a JSON string
get_posting_schedule200_response_instance = GetPostingSchedule200Response.from_json(json)
# print the JSON string representation of the object
print(GetPostingSchedule200Response.to_json())

# convert the object into a dict
get_posting_schedule200_response_dict = get_posting_schedule200_response_instance.to_dict()
# create an instance of GetPostingSchedule200Response from a dict
get_posting_schedule200_response_from_dict = GetPostingSchedule200Response.from_dict(get_posting_schedule200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



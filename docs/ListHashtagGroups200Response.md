# ListHashtagGroups200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**links** | [**PaginationMetaLinks**](PaginationMetaLinks.md) |  | [optional] 
**meta** | [**PaginationMetaMeta**](PaginationMetaMeta.md) |  | [optional] 
**data** | [**List[HashtagGroup]**](HashtagGroup.md) |  | 

## Example

```python
from postboost.models.list_hashtag_groups200_response import ListHashtagGroups200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListHashtagGroups200Response from a JSON string
list_hashtag_groups200_response_instance = ListHashtagGroups200Response.from_json(json)
# print the JSON string representation of the object
print(ListHashtagGroups200Response.to_json())

# convert the object into a dict
list_hashtag_groups200_response_dict = list_hashtag_groups200_response_instance.to_dict()
# create an instance of ListHashtagGroups200Response from a dict
list_hashtag_groups200_response_from_dict = ListHashtagGroups200Response.from_dict(list_hashtag_groups200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# ListMentions200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**links** | [**PaginationMetaLinks**](PaginationMetaLinks.md) |  | [optional] 
**meta** | [**PaginationMetaMeta**](PaginationMetaMeta.md) |  | [optional] 
**data** | [**List[Mention]**](Mention.md) |  | [optional] 

## Example

```python
from postboost.models.list_mentions200_response import ListMentions200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListMentions200Response from a JSON string
list_mentions200_response_instance = ListMentions200Response.from_json(json)
# print the JSON string representation of the object
print(ListMentions200Response.to_json())

# convert the object into a dict
list_mentions200_response_dict = list_mentions200_response_instance.to_dict()
# create an instance of ListMentions200Response from a dict
list_mentions200_response_from_dict = ListMentions200Response.from_dict(list_mentions200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



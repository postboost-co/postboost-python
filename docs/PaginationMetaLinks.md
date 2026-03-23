# PaginationMetaLinks


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**first** | **str** |  | [optional] 
**last** | **str** |  | [optional] 
**prev** | **str** |  | [optional] 
**next** | **str** |  | [optional] 

## Example

```python
from postboost.models.pagination_meta_links import PaginationMetaLinks

# TODO update the JSON string below
json = "{}"
# create an instance of PaginationMetaLinks from a JSON string
pagination_meta_links_instance = PaginationMetaLinks.from_json(json)
# print the JSON string representation of the object
print(PaginationMetaLinks.to_json())

# convert the object into a dict
pagination_meta_links_dict = pagination_meta_links_instance.to_dict()
# create an instance of PaginationMetaLinks from a dict
pagination_meta_links_from_dict = PaginationMetaLinks.from_dict(pagination_meta_links_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# PostWarnings


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**warnings** | [**List[PostWarning]**](PostWarning.md) | Present only when there is at least one warning. | [optional] 

## Example

```python
from postboost.models.post_warnings import PostWarnings

# TODO update the JSON string below
json = "{}"
# create an instance of PostWarnings from a JSON string
post_warnings_instance = PostWarnings.from_json(json)
# print the JSON string representation of the object
print(PostWarnings.to_json())

# convert the object into a dict
post_warnings_dict = post_warnings_instance.to_dict()
# create an instance of PostWarnings from a dict
post_warnings_from_dict = PostWarnings.from_dict(post_warnings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



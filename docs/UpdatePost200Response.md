# UpdatePost200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**warnings** | [**List[PostWarning]**](PostWarning.md) | Present only when there is at least one warning. | [optional] 
**success** | **bool** |  | [optional] 

## Example

```python
from postboost.models.update_post200_response import UpdatePost200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UpdatePost200Response from a JSON string
update_post200_response_instance = UpdatePost200Response.from_json(json)
# print the JSON string representation of the object
print(UpdatePost200Response.to_json())

# convert the object into a dict
update_post200_response_dict = update_post200_response_instance.to_dict()
# create an instance of UpdatePost200Response from a dict
update_post200_response_from_dict = UpdatePost200Response.from_dict(update_post200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



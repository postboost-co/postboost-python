# CreateMention201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**Mention**](Mention.md) |  | [optional] 

## Example

```python
from postboost.models.create_mention201_response import CreateMention201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateMention201Response from a JSON string
create_mention201_response_instance = CreateMention201Response.from_json(json)
# print the JSON string representation of the object
print(CreateMention201Response.to_json())

# convert the object into a dict
create_mention201_response_dict = create_mention201_response_instance.to_dict()
# create an instance of CreateMention201Response from a dict
create_mention201_response_from_dict = CreateMention201Response.from_dict(create_mention201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



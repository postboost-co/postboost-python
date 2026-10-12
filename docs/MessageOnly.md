# MessageOnly


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 

## Example

```python
from postboost.models.message_only import MessageOnly

# TODO update the JSON string below
json = "{}"
# create an instance of MessageOnly from a JSON string
message_only_instance = MessageOnly.from_json(json)
# print the JSON string representation of the object
print(MessageOnly.to_json())

# convert the object into a dict
message_only_dict = message_only_instance.to_dict()
# create an instance of MessageOnly from a dict
message_only_from_dict = MessageOnly.from_dict(message_only_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



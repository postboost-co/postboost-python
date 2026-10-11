# MentionInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**avatar** | **str** |  | [optional] 
**identities** | [**List[MentionIdentityInput]**](MentionIdentityInput.md) |  | [optional] 

## Example

```python
from postboost.models.mention_input import MentionInput

# TODO update the JSON string below
json = "{}"
# create an instance of MentionInput from a JSON string
mention_input_instance = MentionInput.from_json(json)
# print the JSON string representation of the object
print(MentionInput.to_json())

# convert the object into a dict
mention_input_dict = mention_input_instance.to_dict()
# create an instance of MentionInput from a dict
mention_input_from_dict = MentionInput.from_dict(mention_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



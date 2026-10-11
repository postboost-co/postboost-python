# MentionIdentity


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider** | **str** | Mention provider key (network family). | 
**provider_id** | **str** | The profile&#39;s network ID, when resolved. Never accepted from clients. | [optional] 
**handle** | **str** |  | 
**label** | **str** |  | [optional] 

## Example

```python
from postboost.models.mention_identity import MentionIdentity

# TODO update the JSON string below
json = "{}"
# create an instance of MentionIdentity from a JSON string
mention_identity_instance = MentionIdentity.from_json(json)
# print the JSON string representation of the object
print(MentionIdentity.to_json())

# convert the object into a dict
mention_identity_dict = mention_identity_instance.to_dict()
# create an instance of MentionIdentity from a dict
mention_identity_from_dict = MentionIdentity.from_dict(mention_identity_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



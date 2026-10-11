# MentionIdentityInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider** | **str** | Mention provider key. One identity per provider. | 
**handle** | **str** | Profile handle; a leading &#x60;@&#x60; is stripped. | 
**label** | **str** |  | [optional] 
**token** | **str** | Sealed lookup result that names the profile&#39;s network ID. | [optional] 
**account_uuid** | **str** | A connected account of this workspace that names the profile. Wins over &#x60;token&#x60; when both are sent. | [optional] 

## Example

```python
from postboost.models.mention_identity_input import MentionIdentityInput

# TODO update the JSON string below
json = "{}"
# create an instance of MentionIdentityInput from a JSON string
mention_identity_input_instance = MentionIdentityInput.from_json(json)
# print the JSON string representation of the object
print(MentionIdentityInput.to_json())

# convert the object into a dict
mention_identity_input_dict = mention_identity_input_instance.to_dict()
# create an instance of MentionIdentityInput from a dict
mention_identity_input_from_dict = MentionIdentityInput.from_dict(mention_identity_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



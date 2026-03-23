# PostInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**versions** | [**List[PostVersion]**](PostVersion.md) | At least one version with &#x60;is_original: true&#x60; is required. | 
**accounts** | **List[int]** | Account IDs to publish to. | [optional] 
**tags** | **List[int]** | Tag IDs to attach. | [optional] 
**var_date** | **date** |  | [optional] 
**time** | **str** |  | [optional] 
**timezone** | **str** |  | [optional] 
**schedule** | **bool** | Schedule the post for the given date/time. | [optional] 
**schedule_now** | **bool** | Publish immediately. | [optional] 
**queue** | **bool** | Add to the smart publishing queue. | [optional] 

## Example

```python
from postboost.models.post_input import PostInput

# TODO update the JSON string below
json = "{}"
# create an instance of PostInput from a JSON string
post_input_instance = PostInput.from_json(json)
# print the JSON string representation of the object
print(PostInput.to_json())

# convert the object into a dict
post_input_dict = post_input_instance.to_dict()
# create an instance of PostInput from a dict
post_input_from_dict = PostInput.from_dict(post_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



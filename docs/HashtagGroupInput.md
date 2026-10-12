# HashtagGroupInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**content** | **str** |  | 

## Example

```python
from postboost.models.hashtag_group_input import HashtagGroupInput

# TODO update the JSON string below
json = "{}"
# create an instance of HashtagGroupInput from a JSON string
hashtag_group_input_instance = HashtagGroupInput.from_json(json)
# print the JSON string representation of the object
print(HashtagGroupInput.to_json())

# convert the object into a dict
hashtag_group_input_dict = hashtag_group_input_instance.to_dict()
# create an instance of HashtagGroupInput from a dict
hashtag_group_input_from_dict = HashtagGroupInput.from_dict(hashtag_group_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



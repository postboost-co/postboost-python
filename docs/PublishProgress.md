# PublishProgress


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** | Number of accounts the post goes to. | 
**published** | **int** |  | 
**failed** | **int** |  | 

## Example

```python
from postboost.models.publish_progress import PublishProgress

# TODO update the JSON string below
json = "{}"
# create an instance of PublishProgress from a JSON string
publish_progress_instance = PublishProgress.from_json(json)
# print the JSON string representation of the object
print(PublishProgress.to_json())

# convert the object into a dict
publish_progress_dict = publish_progress_instance.to_dict()
# create an instance of PublishProgress from a dict
publish_progress_from_dict = PublishProgress.from_dict(publish_progress_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



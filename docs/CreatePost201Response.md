# CreatePost201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**uuid** | **str** |  | 
**status** | [**PostStatus**](PostStatus.md) |  | 
**publish_progress** | [**PublishProgress**](PublishProgress.md) | Only present while the post is publishing. | [optional] 
**accounts** | [**List[Account]**](Account.md) |  | 
**versions** | [**List[PostVersion]**](PostVersion.md) |  | 
**tags** | [**List[Tag]**](Tag.md) |  | 
**scheduled_at** | **datetime** |  | [optional] 
**published_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | 
**trashed** | **bool** |  | 
**warnings** | [**List[PostWarning]**](PostWarning.md) | Present only when there is at least one warning. | [optional] 

## Example

```python
from postboost.models.create_post201_response import CreatePost201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreatePost201Response from a JSON string
create_post201_response_instance = CreatePost201Response.from_json(json)
# print the JSON string representation of the object
print(CreatePost201Response.to_json())

# convert the object into a dict
create_post201_response_dict = create_post201_response_instance.to_dict()
# create an instance of CreatePost201Response from a dict
create_post201_response_from_dict = CreatePost201Response.from_dict(create_post201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



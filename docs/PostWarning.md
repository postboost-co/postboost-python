# PostWarning

A non-blocking warning on a successful create or update: the post was saved, but something will not behave as you may expect. Log the `code`. - `ai_media_without_disclosure`: the post uses media from the AI image endpoints but   `ai_generated` is `false`, so no network AI label is applied. - `meta_first_comment_unavailable`: a Facebook Page or Instagram first comment cannot   be published yet (Meta is reviewing our access); the post itself publishes. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **str** |  | 
**account_id** | **int** | The account the warning is about; null when it is about the whole post. | 
**message** | **str** |  | 

## Example

```python
from postboost.models.post_warning import PostWarning

# TODO update the JSON string below
json = "{}"
# create an instance of PostWarning from a JSON string
post_warning_instance = PostWarning.from_json(json)
# print the JSON string representation of the object
print(PostWarning.to_json())

# convert the object into a dict
post_warning_dict = post_warning_instance.to_dict()
# create an instance of PostWarning from a dict
post_warning_from_dict = PostWarning.from_dict(post_warning_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



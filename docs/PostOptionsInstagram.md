# PostOptionsInstagram

Instagram options (`instagram` for accounts connected through Facebook, `instagram_standalone` for Instagram Login).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | [optional] [default to 'post']
**collaborators** | **List[str]** | Usernames invited as collaborators (not for stories). | [optional] 
**ai_generated** | **bool** | Instagram&#39;s \&quot;AI info\&quot; label on the post (on the carousel itself for carousels; not for stories). Set by &#x60;ai_generated&#x60;. | [optional] [default to False]

## Example

```python
from postboost.models.post_options_instagram import PostOptionsInstagram

# TODO update the JSON string below
json = "{}"
# create an instance of PostOptionsInstagram from a JSON string
post_options_instagram_instance = PostOptionsInstagram.from_json(json)
# print the JSON string representation of the object
print(PostOptionsInstagram.to_json())

# convert the object into a dict
post_options_instagram_dict = post_options_instagram_instance.to_dict()
# create an instance of PostOptionsInstagram from a dict
post_options_instagram_from_dict = PostOptionsInstagram.from_dict(post_options_instagram_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# PostInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**versions** | [**List[PostVersion]**](PostVersion.md) | At least one version with &#x60;is_original: true&#x60; is required. | 
**accounts** | **List[int]** | Account IDs to publish to. | [optional] 
**tags** | **List[int]** | Tag IDs to attach. | [optional] 
**var_date** | **date** |  | [optional] 
**time** | **str** |  | [optional] 
**timezone** | **str** | Timezone &#x60;date&#x60;, &#x60;time&#x60; and &#x60;accounts_schedule&#x60; are read in. Defaults to the workspace timezone. | [optional] 
**accounts_schedule** | [**List[AccountSchedule]**](AccountSchedule.md) | Per-account departure times. When omitted on update, accounts keep their offsets from the post time. | [optional] 
**schedule** | **bool** | Schedule the post for the given date/time. | [optional] 
**schedule_now** | **bool** | Publish immediately. | [optional] 
**queue** | **bool** | Add to the smart publishing queue. | [optional] 
**ai_generated** | **bool** | Declares the post AI-generated (or, with &#x60;false&#x60;, not). PostBoost sets each network&#39;s own AI label: TikTok&#39;s &#x60;is_aigc&#x60; for every TikTok account in &#x60;accounts&#x60;, Instagram&#39;s \&quot;AI info\&quot; label (&#x60;instagram.ai_generated&#x60;) and YouTube&#39;s synthetic-media disclosure (&#x60;youtube.contains_synthetic_media&#x60;). The other networks have no API label. The response carries &#x60;X-AI-Disclosure: applied&#x60; when every network with a label got it. When omitted, a post that attaches images made by the AI image endpoints is labelled automatically. See the AI disclosure guide.  | [optional] 
**allow_duplicate** | **bool** | Skip the duplicate guard. By default the API refuses (&#x60;409&#x60;, &#x60;code: duplicate_post&#x60;) content that matches a post created for the same account in the last 24 hours. The header &#x60;X-Allow-Duplicate: true&#x60; does the same.  | [optional] [default to False]

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



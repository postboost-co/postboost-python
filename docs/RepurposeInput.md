# RepurposeInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source_type** | **str** |  | 
**url** | **str** | Article URL (&#x60;url&#x60;) or YouTube video URL (&#x60;youtube&#x60;). For &#x60;text&#x60;, an optional link to mention. | [optional] 
**pdf_url** | **str** | Public URL of a PDF (&#x60;pdf&#x60;), at most 20 MB. | [optional] 
**title** | **str** | Required for &#x60;text&#x60;. For &#x60;youtube&#x60;, overrides the video title. | [optional] 
**text** | **str** | Required for &#x60;text&#x60;. Long sources are cut to about 12,000 characters. | [optional] 
**transcript** | **str** | Video transcript for &#x60;youtube&#x60;. | [optional] 
**platforms** | **List[str]** | Limit to connected accounts of these networks. Ignored when &#x60;account_ids&#x60; is set. | [optional] 
**account_ids** | **List[int]** | Target accounts. Default is every connected account. | [optional] 
**tone** | **str** |  | [optional] [default to 'engaging']
**content_length** | **str** |  | [optional] [default to 'medium']
**hashtags** | **str** |  | [optional] [default to 'few']
**cta** | **str** |  | [optional] [default to 'none']
**language** | **str** |  | [optional] [default to 'auto']
**custom_instructions** | **str** |  | [optional] 
**carousel** | **bool** | Render carousel slides (one extra AI credit for the outline). | [optional] [default to True]
**slide_count** | **int** | Total slides including the hook and call-to-action slides. | [optional] [default to 7]
**theme** | [**RepurposeInputTheme**](RepurposeInputTheme.md) |  | [optional] 
**create_post** | **bool** | Create the draft post. &#x60;false&#x60; returns captions and slides only. | [optional] [default to True]
**use_brand_voice** | **bool** |  | [optional] [default to True]
**var_async** | **bool** | Answer &#x60;202&#x60; with a run id right away instead of waiting up to 20 seconds for the result. | [optional] [default to False]

## Example

```python
from postboost.models.repurpose_input import RepurposeInput

# TODO update the JSON string below
json = "{}"
# create an instance of RepurposeInput from a JSON string
repurpose_input_instance = RepurposeInput.from_json(json)
# print the JSON string representation of the object
print(RepurposeInput.to_json())

# convert the object into a dict
repurpose_input_dict = repurpose_input_instance.to_dict()
# create an instance of RepurposeInput from a dict
repurpose_input_from_dict = RepurposeInput.from_dict(repurpose_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# BrandVoiceMeta


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**brand_voice_applied** | **bool** | Whether the workspace brand voice shaped this result. | 

## Example

```python
from postboost.models.brand_voice_meta import BrandVoiceMeta

# TODO update the JSON string below
json = "{}"
# create an instance of BrandVoiceMeta from a JSON string
brand_voice_meta_instance = BrandVoiceMeta.from_json(json)
# print the JSON string representation of the object
print(BrandVoiceMeta.to_json())

# convert the object into a dict
brand_voice_meta_dict = brand_voice_meta_instance.to_dict()
# create an instance of BrandVoiceMeta from a dict
brand_voice_meta_from_dict = BrandVoiceMeta.from_dict(brand_voice_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



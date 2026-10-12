# RepurposeContent200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**RepurposeResult**](RepurposeResult.md) |  | 
**meta** | [**BrandVoiceMeta**](BrandVoiceMeta.md) |  | 

## Example

```python
from postboost.models.repurpose_content200_response import RepurposeContent200Response

# TODO update the JSON string below
json = "{}"
# create an instance of RepurposeContent200Response from a JSON string
repurpose_content200_response_instance = RepurposeContent200Response.from_json(json)
# print the JSON string representation of the object
print(RepurposeContent200Response.to_json())

# convert the object into a dict
repurpose_content200_response_dict = repurpose_content200_response_instance.to_dict()
# create an instance of RepurposeContent200Response from a dict
repurpose_content200_response_from_dict = RepurposeContent200Response.from_dict(repurpose_content200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



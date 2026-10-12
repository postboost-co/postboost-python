# RepurposeResultSource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**title** | **str** |  | 
**url** | **str** |  | 

## Example

```python
from postboost.models.repurpose_result_source import RepurposeResultSource

# TODO update the JSON string below
json = "{}"
# create an instance of RepurposeResultSource from a JSON string
repurpose_result_source_instance = RepurposeResultSource.from_json(json)
# print the JSON string representation of the object
print(RepurposeResultSource.to_json())

# convert the object into a dict
repurpose_result_source_dict = repurpose_result_source_instance.to_dict()
# create an instance of RepurposeResultSource from a dict
repurpose_result_source_from_dict = RepurposeResultSource.from_dict(repurpose_result_source_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# RepurposeRun


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**run_id** | **int** |  | 
**status** | **str** |  | 
**error** | **str** | Why the run failed. | 
**post_uuid** | **str** | The draft post, once created. | 
**credits_used** | **int** |  | 
**result** | [**RepurposeResult**](RepurposeResult.md) |  | 

## Example

```python
from postboost.models.repurpose_run import RepurposeRun

# TODO update the JSON string below
json = "{}"
# create an instance of RepurposeRun from a JSON string
repurpose_run_instance = RepurposeRun.from_json(json)
# print the JSON string representation of the object
print(RepurposeRun.to_json())

# convert the object into a dict
repurpose_run_dict = repurpose_run_instance.to_dict()
# create an instance of RepurposeRun from a dict
repurpose_run_from_dict = RepurposeRun.from_dict(repurpose_run_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



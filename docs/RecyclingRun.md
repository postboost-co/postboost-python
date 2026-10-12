# RecyclingRun


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**status** | **str** |  | 
**reason** | **str** | Why the run skipped or failed; on &#x60;created&#x60;, a note such as &#x60;x_skipped_identical_text&#x60;. | 
**source_post_uuid** | **str** |  | 
**created_post_uuid** | **str** |  | 
**created_at** | **datetime** |  | 

## Example

```python
from postboost.models.recycling_run import RecyclingRun

# TODO update the JSON string below
json = "{}"
# create an instance of RecyclingRun from a JSON string
recycling_run_instance = RecyclingRun.from_json(json)
# print the JSON string representation of the object
print(RecyclingRun.to_json())

# convert the object into a dict
recycling_run_dict = recycling_run_instance.to_dict()
# create an instance of RecyclingRun from a dict
recycling_run_from_dict = RecyclingRun.from_dict(recycling_run_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# RepurposeRunAccepted


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**run_id** | **int** |  | 
**status** | **str** |  | 
**status_url** | **str** | The &#x60;getRepurposeRun&#x60; URL for this run. | 

## Example

```python
from postboost.models.repurpose_run_accepted import RepurposeRunAccepted

# TODO update the JSON string below
json = "{}"
# create an instance of RepurposeRunAccepted from a JSON string
repurpose_run_accepted_instance = RepurposeRunAccepted.from_json(json)
# print the JSON string representation of the object
print(RepurposeRunAccepted.to_json())

# convert the object into a dict
repurpose_run_accepted_dict = repurpose_run_accepted_instance.to_dict()
# create an instance of RepurposeRunAccepted from a dict
repurpose_run_accepted_from_dict = RepurposeRunAccepted.from_dict(repurpose_run_accepted_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



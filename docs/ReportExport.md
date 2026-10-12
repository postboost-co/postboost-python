# ReportExport


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**uuid** | **str** |  | 
**format** | **str** |  | 
**dataset** | **str** |  | 
**period** | **str** |  | 
**date_from** | **date** |  | 
**date_to** | **date** |  | 
**account_ids** | **List[int]** |  | 
**status** | **str** |  | 
**error** | **str** |  | 
**bytes** | **int** |  | 
**download_url** | **str** | Authenticated download URL while the file is available. | 
**created_at** | **datetime** |  | 
**expires_at** | **datetime** |  | 

## Example

```python
from postboost.models.report_export import ReportExport

# TODO update the JSON string below
json = "{}"
# create an instance of ReportExport from a JSON string
report_export_instance = ReportExport.from_json(json)
# print the JSON string representation of the object
print(ReportExport.to_json())

# convert the object into a dict
report_export_dict = report_export_instance.to_dict()
# create an instance of ReportExport from a dict
report_export_from_dict = ReportExport.from_dict(report_export_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



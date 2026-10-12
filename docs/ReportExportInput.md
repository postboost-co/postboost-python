# ReportExportInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**format** | **str** |  | 
**dataset** | **str** | CSV rows; default &#x60;posts&#x60;. Ignored for PDF. | [optional] 
**period** | **str** | Default &#x60;last_month&#x60;. Ignored when &#x60;date_from&#x60; and &#x60;date_to&#x60; are sent. | [optional] 
**date_from** | **date** |  | [optional] 
**date_to** | **date** | At most 366 days after &#x60;date_from&#x60;. | [optional] 
**account_ids** | **List[int]** | Limit the report to these accounts; default all. | [optional] 

## Example

```python
from postboost.models.report_export_input import ReportExportInput

# TODO update the JSON string below
json = "{}"
# create an instance of ReportExportInput from a JSON string
report_export_input_instance = ReportExportInput.from_json(json)
# print the JSON string representation of the object
print(ReportExportInput.to_json())

# convert the object into a dict
report_export_input_dict = report_export_input_instance.to_dict()
# create an instance of ReportExportInput from a dict
report_export_input_from_dict = ReportExportInput.from_dict(report_export_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



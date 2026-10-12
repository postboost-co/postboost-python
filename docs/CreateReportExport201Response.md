# CreateReportExport201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**ReportExport**](ReportExport.md) |  | 

## Example

```python
from postboost.models.create_report_export201_response import CreateReportExport201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateReportExport201Response from a JSON string
create_report_export201_response_instance = CreateReportExport201Response.from_json(json)
# print the JSON string representation of the object
print(CreateReportExport201Response.to_json())

# convert the object into a dict
create_report_export201_response_dict = create_report_export201_response_instance.to_dict()
# create an instance of CreateReportExport201Response from a dict
create_report_export201_response_from_dict = CreateReportExport201Response.from_dict(create_report_export201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



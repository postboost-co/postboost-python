# ReportBranding


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**display_name** | **str** |  | 
**primary_color** | **str** |  | 
**footer_text** | **str** |  | 
**show_powered_by** | **bool** |  | 
**has_logo** | **bool** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from postboost.models.report_branding import ReportBranding

# TODO update the JSON string below
json = "{}"
# create an instance of ReportBranding from a JSON string
report_branding_instance = ReportBranding.from_json(json)
# print the JSON string representation of the object
print(ReportBranding.to_json())

# convert the object into a dict
report_branding_dict = report_branding_instance.to_dict()
# create an instance of ReportBranding from a dict
report_branding_from_dict = ReportBranding.from_dict(report_branding_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



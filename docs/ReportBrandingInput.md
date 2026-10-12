# ReportBrandingInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**display_name** | **str** | Name in the report header; default the workspace name. | [optional] 
**primary_color** | **str** |  | [optional] 
**footer_text** | **str** |  | [optional] 
**show_powered_by** | **bool** | Show \&quot;Generated with PostBoost\&quot; in the footer. | [optional] 

## Example

```python
from postboost.models.report_branding_input import ReportBrandingInput

# TODO update the JSON string below
json = "{}"
# create an instance of ReportBrandingInput from a JSON string
report_branding_input_instance = ReportBrandingInput.from_json(json)
# print the JSON string representation of the object
print(ReportBrandingInput.to_json())

# convert the object into a dict
report_branding_input_dict = report_branding_input_instance.to_dict()
# create an instance of ReportBrandingInput from a dict
report_branding_input_from_dict = ReportBrandingInput.from_dict(report_branding_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



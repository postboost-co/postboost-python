# FreeToolGenerateQrCodeRequestUtm

UTM tags added to an http(s) link, the same way as buildUtmUrl.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source** | **str** |  | [optional] 
**medium** | **str** |  | [optional] 
**campaign** | **str** |  | [optional] 
**term** | **str** |  | [optional] 
**content** | **str** |  | [optional] 

## Example

```python
from postboost.models.free_tool_generate_qr_code_request_utm import FreeToolGenerateQrCodeRequestUtm

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateQrCodeRequestUtm from a JSON string
free_tool_generate_qr_code_request_utm_instance = FreeToolGenerateQrCodeRequestUtm.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateQrCodeRequestUtm.to_json())

# convert the object into a dict
free_tool_generate_qr_code_request_utm_dict = free_tool_generate_qr_code_request_utm_instance.to_dict()
# create an instance of FreeToolGenerateQrCodeRequestUtm from a dict
free_tool_generate_qr_code_request_utm_from_dict = FreeToolGenerateQrCodeRequestUtm.from_dict(free_tool_generate_qr_code_request_utm_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



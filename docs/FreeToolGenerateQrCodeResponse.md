# FreeToolGenerateQrCodeResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | **str** | The exact string encoded in the code (the link with its UTM tags). | [optional] 
**svg** | **str** | The QR code as an SVG document. | [optional] 
**warnings** | **List[str]** |  | [optional] 

## Example

```python
from postboost.models.free_tool_generate_qr_code_response import FreeToolGenerateQrCodeResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateQrCodeResponse from a JSON string
free_tool_generate_qr_code_response_instance = FreeToolGenerateQrCodeResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateQrCodeResponse.to_json())

# convert the object into a dict
free_tool_generate_qr_code_response_dict = free_tool_generate_qr_code_response_instance.to_dict()
# create an instance of FreeToolGenerateQrCodeResponse from a dict
free_tool_generate_qr_code_response_from_dict = FreeToolGenerateQrCodeResponse.from_dict(free_tool_generate_qr_code_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



# FreeToolGenerateQrCodeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | **str** | The link or text to encode. | 
**utm** | [**FreeToolGenerateQrCodeRequestUtm**](FreeToolGenerateQrCodeRequestUtm.md) |  | [optional] 
**error_correction** | **str** | How much of the code can be damaged and still scan: L 7%, M 15%, Q 25%, H 30%. | [optional] [default to 'M']
**size** | **int** | Width and height of the SVG in pixels. | [optional] [default to 512]
**foreground** | **str** | Colour of the modules, #RRGGBB. | [optional] [default to '#000000']
**background** | **str** | Background colour, #RRGGBB. | [optional] [default to '#FFFFFF']

## Example

```python
from postboost.models.free_tool_generate_qr_code_request import FreeToolGenerateQrCodeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGenerateQrCodeRequest from a JSON string
free_tool_generate_qr_code_request_instance = FreeToolGenerateQrCodeRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolGenerateQrCodeRequest.to_json())

# convert the object into a dict
free_tool_generate_qr_code_request_dict = free_tool_generate_qr_code_request_instance.to_dict()
# create an instance of FreeToolGenerateQrCodeRequest from a dict
free_tool_generate_qr_code_request_from_dict = FreeToolGenerateQrCodeRequest.from_dict(free_tool_generate_qr_code_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



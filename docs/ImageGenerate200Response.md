# ImageGenerate200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**ImageGenerationResponse**](ImageGenerationResponse.md) |  | 

## Example

```python
from postboost.models.image_generate200_response import ImageGenerate200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ImageGenerate200Response from a JSON string
image_generate200_response_instance = ImageGenerate200Response.from_json(json)
# print the JSON string representation of the object
print(ImageGenerate200Response.to_json())

# convert the object into a dict
image_generate200_response_dict = image_generate200_response_instance.to_dict()
# create an instance of ImageGenerate200Response from a dict
image_generate200_response_from_dict = ImageGenerate200Response.from_dict(image_generate200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



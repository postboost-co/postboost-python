# ImagePromptResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prompt** | **str** |  | 

## Example

```python
from postboost.models.image_prompt_response import ImagePromptResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ImagePromptResponse from a JSON string
image_prompt_response_instance = ImagePromptResponse.from_json(json)
# print the JSON string representation of the object
print(ImagePromptResponse.to_json())

# convert the object into a dict
image_prompt_response_dict = image_prompt_response_instance.to_dict()
# create an instance of ImagePromptResponse from a dict
image_prompt_response_from_dict = ImagePromptResponse.from_dict(image_prompt_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



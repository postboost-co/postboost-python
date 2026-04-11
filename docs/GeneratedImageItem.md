# GeneratedImageItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**media_id** | **int** |  | 
**url** | **str** |  | 
**thumb_url** | **str** |  | 

## Example

```python
from postboost.models.generated_image_item import GeneratedImageItem

# TODO update the JSON string below
json = "{}"
# create an instance of GeneratedImageItem from a JSON string
generated_image_item_instance = GeneratedImageItem.from_json(json)
# print the JSON string representation of the object
print(GeneratedImageItem.to_json())

# convert the object into a dict
generated_image_item_dict = generated_image_item_instance.to_dict()
# create an instance of GeneratedImageItem from a dict
generated_image_item_from_dict = GeneratedImageItem.from_dict(generated_image_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



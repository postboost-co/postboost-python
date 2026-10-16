# FreeToolPreviewPostResponseNetworksInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | [optional] 
**count** | **int** |  | [optional] 
**limit** | **int** |  | [optional] 
**over** | **bool** |  | [optional] 
**preview** | **str** | What the feed shows before the \&quot;more\&quot; link (approximate; varies by device). | [optional] 
**folded** | **bool** |  | [optional] 
**min_ratio** | **str** | Tallest image ratio the feed shows uncropped (Instagram: the chosen ratio). Taller images are cropped from the centre. | [optional] 
**max_ratio** | **str** | Widest image ratio the feed shows uncropped (Instagram: the chosen ratio). Wider images are cropped from the centre. | [optional] 
**display_ratio** | **float** | Width / height the card shows the image at, 2 decimals. Only when image_width and image_height are given. | [optional] 
**cropped** | **bool** | Whether the card crops the image. Only when image_width and image_height are given. | [optional] 

## Example

```python
from postboost.models.free_tool_preview_post_response_networks_inner import FreeToolPreviewPostResponseNetworksInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPreviewPostResponseNetworksInner from a JSON string
free_tool_preview_post_response_networks_inner_instance = FreeToolPreviewPostResponseNetworksInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolPreviewPostResponseNetworksInner.to_json())

# convert the object into a dict
free_tool_preview_post_response_networks_inner_dict = free_tool_preview_post_response_networks_inner_instance.to_dict()
# create an instance of FreeToolPreviewPostResponseNetworksInner from a dict
free_tool_preview_post_response_networks_inner_from_dict = FreeToolPreviewPostResponseNetworksInner.from_dict(free_tool_preview_post_response_networks_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



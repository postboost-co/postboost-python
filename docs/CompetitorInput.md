# CompetitorInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **int** | Your Instagram account &#x60;id&#x60; (connected through a Facebook Page) used to look the competitor up. | 
**username** | **str** | Instagram username, with or without &#x60;@&#x60;. | 

## Example

```python
from postboost.models.competitor_input import CompetitorInput

# TODO update the JSON string below
json = "{}"
# create an instance of CompetitorInput from a JSON string
competitor_input_instance = CompetitorInput.from_json(json)
# print the JSON string representation of the object
print(CompetitorInput.to_json())

# convert the object into a dict
competitor_input_dict = competitor_input_instance.to_dict()
# create an instance of CompetitorInput from a dict
competitor_input_from_dict = CompetitorInput.from_dict(competitor_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



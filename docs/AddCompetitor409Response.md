# AddCompetitor409Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**competitor_id** | **int** |  | [optional] 

## Example

```python
from postboost.models.add_competitor409_response import AddCompetitor409Response

# TODO update the JSON string below
json = "{}"
# create an instance of AddCompetitor409Response from a JSON string
add_competitor409_response_instance = AddCompetitor409Response.from_json(json)
# print the JSON string representation of the object
print(AddCompetitor409Response.to_json())

# convert the object into a dict
add_competitor409_response_dict = add_competitor409_response_instance.to_dict()
# create an instance of AddCompetitor409Response from a dict
add_competitor409_response_from_dict = AddCompetitor409Response.from_dict(add_competitor409_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



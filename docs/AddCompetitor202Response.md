# AddCompetitor202Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**Competitor**](Competitor.md) |  | 
**status** | **str** |  | 

## Example

```python
from postboost.models.add_competitor202_response import AddCompetitor202Response

# TODO update the JSON string below
json = "{}"
# create an instance of AddCompetitor202Response from a JSON string
add_competitor202_response_instance = AddCompetitor202Response.from_json(json)
# print the JSON string representation of the object
print(AddCompetitor202Response.to_json())

# convert the object into a dict
add_competitor202_response_dict = add_competitor202_response_instance.to_dict()
# create an instance of AddCompetitor202Response from a dict
add_competitor202_response_from_dict = AddCompetitor202Response.from_dict(add_competitor202_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



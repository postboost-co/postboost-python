# ResellerClientInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 

## Example

```python
from postboost.models.reseller_client_input import ResellerClientInput

# TODO update the JSON string below
json = "{}"
# create an instance of ResellerClientInput from a JSON string
reseller_client_input_instance = ResellerClientInput.from_json(json)
# print the JSON string representation of the object
print(ResellerClientInput.to_json())

# convert the object into a dict
reseller_client_input_dict = reseller_client_input_instance.to_dict()
# create an instance of ResellerClientInput from a dict
reseller_client_input_from_dict = ResellerClientInput.from_dict(reseller_client_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



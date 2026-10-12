# CreateResellerClient201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | [**ResellerClient**](ResellerClient.md) |  | 

## Example

```python
from postboost.models.create_reseller_client201_response import CreateResellerClient201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateResellerClient201Response from a JSON string
create_reseller_client201_response_instance = CreateResellerClient201Response.from_json(json)
# print the JSON string representation of the object
print(CreateResellerClient201Response.to_json())

# convert the object into a dict
create_reseller_client201_response_dict = create_reseller_client201_response_instance.to_dict()
# create an instance of CreateResellerClient201Response from a dict
create_reseller_client201_response_from_dict = CreateResellerClient201Response.from_dict(create_reseller_client201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



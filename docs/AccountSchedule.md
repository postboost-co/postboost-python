# AccountSchedule


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **int** | ID of one of the post&#39;s accounts. Entries for accounts the post does not carry are ignored. | 
**var_date** | **date** |  | 
**time** | **str** | H:i, read in the request &#x60;timezone&#x60;. Must not be in the past. | 

## Example

```python
from postboost.models.account_schedule import AccountSchedule

# TODO update the JSON string below
json = "{}"
# create an instance of AccountSchedule from a JSON string
account_schedule_instance = AccountSchedule.from_json(json)
# print the JSON string representation of the object
print(AccountSchedule.to_json())

# convert the object into a dict
account_schedule_dict = account_schedule_instance.to_dict()
# create an instance of AccountSchedule from a dict
account_schedule_from_dict = AccountSchedule.from_dict(account_schedule_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



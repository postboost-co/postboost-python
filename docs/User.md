# User


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**name** | **str** |  | 
**email** | **str** |  | 
**avatar** | **str** | URL of the user&#39;s avatar, or null when none is set. | [optional] 
**is_admin** | **bool** |  | 
**email_verified_at** | **str** | Display string in the configured timezone and clock: &#x60;M j, H:i&#x60; this year, &#x60;M j, Y, H:i&#x60; otherwise (12-hour setting: &#x60;h:ia&#x60;), not RFC 3339. | [optional] 
**created_at** | **str** | Display string in the configured timezone and clock: &#x60;M j, H:i&#x60; this year, &#x60;M j, Y, H:i&#x60; otherwise (12-hour setting: &#x60;h:ia&#x60;), not RFC 3339. | 

## Example

```python
from postboost.models.user import User

# TODO update the JSON string below
json = "{}"
# create an instance of User from a JSON string
user_instance = User.from_json(json)
# print the JSON string representation of the object
print(User.to_json())

# convert the object into a dict
user_dict = user_instance.to_dict()
# create an instance of User from a dict
user_from_dict = User.from_dict(user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



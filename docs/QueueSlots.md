# QueueSlots


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slots** | **List[Dict[str, object]]** | Upcoming posting times and scheduled posts, in order. | 
**next_cursor** | **str** | Pass as &#x60;after&#x60; for the next page; null at the end. | 

## Example

```python
from postboost.models.queue_slots import QueueSlots

# TODO update the JSON string below
json = "{}"
# create an instance of QueueSlots from a JSON string
queue_slots_instance = QueueSlots.from_json(json)
# print the JSON string representation of the object
print(QueueSlots.to_json())

# convert the object into a dict
queue_slots_dict = queue_slots_instance.to_dict()
# create an instance of QueueSlots from a dict
queue_slots_from_dict = QueueSlots.from_dict(queue_slots_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



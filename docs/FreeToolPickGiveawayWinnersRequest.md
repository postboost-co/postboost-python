# FreeToolPickGiveawayWinnersRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**entrants** | [**List[FreeToolPickGiveawayWinnersRequestEntrantsInner]**](FreeToolPickGiveawayWinnersRequestEntrantsInner.md) | The comments, one item each. The request body is capped at 128 KB. | 
**seed** | **str** | The secret seed, 64 hex characters (32 bytes), whose fingerprint you published before the entries closed. Without it, a seed is generated and pre_committed is false. The steps of the draw (pb-draw-v1) and a test vector are on the web tool page. | [optional] 
**one_per_person** | **bool** | Count each username once. Off: every comment is an entry, so one person can win more than once. | [optional] [default to True]
**keywords** | **List[str]** | Keep only comments that contain at least one of these, case-insensitive. | [optional] [default to []]
**min_mentions** | **int** | Keep only comments that tag at least this many other @handles. | [optional] [default to 0]
**exclude** | **List[str]** | Usernames to leave out of the draw, such as the host account. | [optional] [default to []]
**winners** | **int** |  | [optional] [default to 1]
**alternates** | **int** | Runners-up drawn after the winners, in order. | [optional] [default to 0]

## Example

```python
from postboost.models.free_tool_pick_giveaway_winners_request import FreeToolPickGiveawayWinnersRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPickGiveawayWinnersRequest from a JSON string
free_tool_pick_giveaway_winners_request_instance = FreeToolPickGiveawayWinnersRequest.from_json(json)
# print the JSON string representation of the object
print(FreeToolPickGiveawayWinnersRequest.to_json())

# convert the object into a dict
free_tool_pick_giveaway_winners_request_dict = free_tool_pick_giveaway_winners_request_instance.to_dict()
# create an instance of FreeToolPickGiveawayWinnersRequest from a dict
free_tool_pick_giveaway_winners_request_from_dict = FreeToolPickGiveawayWinnersRequest.from_dict(free_tool_pick_giveaway_winners_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



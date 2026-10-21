# FreeToolPickGiveawayWinnersResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**winners** | **List[str]** | Entrant keys in the drawn order. | [optional] 
**alternates** | **List[str]** | Entrant keys drawn after the winners, in order. | [optional] 
**entrants_before** | **int** | Comments received. | [optional] 
**entrants_after** | **int** | Entries left after the filters: the length of entrant_list. | [optional] 
**entrant_list** | **List[str]** | The canonical entrant list to publish: keys sorted by UTF-8 bytes. Joined with \&quot;\\n\&quot; it is what entrants_hash hashes. | [optional] 
**entrants_hash** | **str** | SHA-256 (hex) of the canonical entrant list. | [optional] 
**fingerprint** | **str** | SHA-256 (hex) of the seed bytes: what to publish before the entries close. | [optional] 
**seed** | **str** | The seed used, lowercase hex. Publish it after the draw. | [optional] 
**pre_committed** | **bool** | False when the seed was generated for this draw, so no fingerprint could be published before it. | [optional] 
**algorithm** | **str** |  | [optional] 
**warnings** | [**List[FreeToolCheckPostResponseNetworksInnerErrorsInner]**](FreeToolCheckPostResponseNetworksInnerErrorsInner.md) | Codes: not_enough_entrants, not_pre_committed. | [optional] 

## Example

```python
from postboost.models.free_tool_pick_giveaway_winners_response import FreeToolPickGiveawayWinnersResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolPickGiveawayWinnersResponse from a JSON string
free_tool_pick_giveaway_winners_response_instance = FreeToolPickGiveawayWinnersResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolPickGiveawayWinnersResponse.to_json())

# convert the object into a dict
free_tool_pick_giveaway_winners_response_dict = free_tool_pick_giveaway_winners_response_instance.to_dict()
# create an instance of FreeToolPickGiveawayWinnersResponse from a dict
free_tool_pick_giveaway_winners_response_from_dict = FreeToolPickGiveawayWinnersResponse.from_dict(free_tool_pick_giveaway_winners_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



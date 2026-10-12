# ChannelAccount

A connected Telegram, Discord or Slack channel. Same fields as `Account`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**uuid** | **str** |  | 
**name** | **str** |  | 
**username** | **str** | Telegram public channel username; null for private channels, Discord and Slack. | [optional] 
**image** | **str** |  | [optional] 
**provider** | **str** |  | 
**data** | **object** | Provider metadata (Telegram &#x60;chat_id&#x60;, Discord &#x60;channel_id&#x60;/&#x60;guild_id&#x60;, Slack &#x60;team_id&#x60;). | 
**authorized** | **bool** |  | 
**profile_url** | **str** |  | [optional] 
**created_at** | **str** |  | 

## Example

```python
from postboost.models.channel_account import ChannelAccount

# TODO update the JSON string below
json = "{}"
# create an instance of ChannelAccount from a JSON string
channel_account_instance = ChannelAccount.from_json(json)
# print the JSON string representation of the object
print(ChannelAccount.to_json())

# convert the object into a dict
channel_account_dict = channel_account_instance.to_dict()
# create an instance of ChannelAccount from a dict
channel_account_from_dict = ChannelAccount.from_dict(channel_account_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



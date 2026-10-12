# ConnectChannelInput

Fields depend on the provider in the path; see the operation description.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bot_token** | **str** | Telegram only. Bot token from @BotFather. | [optional] 
**chat** | **str** | Telegram only. Channel &#x60;@username&#x60; or numeric chat id. | [optional] 
**webhook_url** | **str** | Discord or Slack incoming webhook URL. | [optional] 
**name** | **str** | Slack only. Display name for the channel (Slack webhooks do not report one). | [optional] 

## Example

```python
from postboost.models.connect_channel_input import ConnectChannelInput

# TODO update the JSON string below
json = "{}"
# create an instance of ConnectChannelInput from a JSON string
connect_channel_input_instance = ConnectChannelInput.from_json(json)
# print the JSON string representation of the object
print(ConnectChannelInput.to_json())

# convert the object into a dict
connect_channel_input_dict = connect_channel_input_instance.to_dict()
# create an instance of ConnectChannelInput from a dict
connect_channel_input_from_dict = ConnectChannelInput.from_dict(connect_channel_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



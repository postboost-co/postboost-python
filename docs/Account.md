# Account


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** |  | 
**uuid** | **str** |  | 
**name** | **str** |  | 
**username** | **str** |  | 
**image** | **str** |  | [optional] 
**provider** | **str** | Network key. Known values: &#x60;twitter&#x60;, &#x60;facebook_page&#x60;, &#x60;instagram&#x60;, &#x60;instagram_standalone&#x60;, &#x60;threads&#x60;, &#x60;linkedin&#x60;, &#x60;linkedin_page&#x60;, &#x60;tiktok&#x60;, &#x60;youtube&#x60;, &#x60;pinterest&#x60;, &#x60;gbp&#x60;, &#x60;bluesky&#x60;, &#x60;mastodon&#x60;, &#x60;pixelfed&#x60;, &#x60;telegram&#x60;, &#x60;discord&#x60;, &#x60;slack&#x60;. New networks add new keys, so treat unknown values as valid.  | 
**data** | **object** | Provider-specific metadata. | 
**authorized** | **bool** |  | 
**profile_url** | **str** | Public URL of the account&#39;s profile on the network, when known. | [optional] 
**publish_status** | **str** | Only present when the account is embedded in a post. Publishing state of this account for the post. | [optional] 
**published_parts** | **int** | Only present when the account is embedded in a post. How many parts (for example thread items or a first comment) are live on the network. | [optional] 
**external_url** | **str** | Only present when the account is embedded in a post. URL of the published post on the network, null until it is live. | [optional] 
**provider_post_id** | **str** | Only present when the account is embedded in a post. The network&#39;s own ID of the published post (for example a LinkedIn share URN or a tweet ID), null until it is live. | [optional] 
**errors** | [**List[AccountErrorsInner]**](AccountErrorsInner.md) | Only present when the account is embedded in a post. Why publishing to this account failed. A raw network error is stored as two entries: a readable line (&#x60;\&quot;&lt;Network&gt;: &lt;message&gt; (code &lt;code&gt;)\&quot;&#x60;) and an object &#x60;{platform, code, message, raw}&#x60; with the network&#39;s original response in &#x60;raw&#x60;. Other failures are a single readable string.  | [optional] 
**created_at** | **str** | UTC, formatted &#x60;Y-m-d H:i:s&#x60;. | 

## Example

```python
from postboost.models.account import Account

# TODO update the JSON string below
json = "{}"
# create an instance of Account from a JSON string
account_instance = Account.from_json(json)
# print the JSON string representation of the object
print(Account.to_json())

# convert the object into a dict
account_dict = account_instance.to_dict()
# create an instance of Account from a dict
account_from_dict = Account.from_dict(account_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



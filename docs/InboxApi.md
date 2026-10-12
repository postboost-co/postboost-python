# postboost.InboxApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**approve_inbox_reply_draft**](InboxApi.md#approve_inbox_reply_draft) | **POST** /{workspaceUuid}/inbox/drafts/{draftId}/approve | Approve and send a reply draft
[**create_inbox_reply_draft**](InboxApi.md#create_inbox_reply_draft) | **POST** /{workspaceUuid}/inbox/conversations/{conversationId}/drafts | Draft a reply
[**delete_inbox_reply_draft**](InboxApi.md#delete_inbox_reply_draft) | **DELETE** /{workspaceUuid}/inbox/drafts/{draftId} | Withdraw a reply draft
[**get_inbox_conversation**](InboxApi.md#get_inbox_conversation) | **GET** /{workspaceUuid}/inbox/conversations/{conversationId} | Get an inbox conversation
[**get_inbox_reply_draft**](InboxApi.md#get_inbox_reply_draft) | **GET** /{workspaceUuid}/inbox/drafts/{draftId} | Get a reply draft
[**list_inbox_conversations**](InboxApi.md#list_inbox_conversations) | **GET** /{workspaceUuid}/inbox/conversations | List inbox conversations
[**list_inbox_reply_drafts**](InboxApi.md#list_inbox_reply_drafts) | **GET** /{workspaceUuid}/inbox/drafts | List reply drafts
[**reject_inbox_reply_draft**](InboxApi.md#reject_inbox_reply_draft) | **POST** /{workspaceUuid}/inbox/drafts/{draftId}/reject | Reject a reply draft
[**update_inbox_conversation**](InboxApi.md#update_inbox_conversation) | **PATCH** /{workspaceUuid}/inbox/conversations/{conversationId} | Update an inbox conversation
[**update_inbox_reply_draft**](InboxApi.md#update_inbox_reply_draft) | **PUT** /{workspaceUuid}/inbox/drafts/{draftId} | Edit a reply draft


# **approve_inbox_reply_draft**
> CreateInboxReplyDraft201Response approve_inbox_reply_draft(workspace_uuid, draft_id, inbox_reply_draft_approve=inbox_reply_draft_approve)

Approve and send a reply draft

Sends the draft to the network (optionally with an edited `body`). Ends as `sent`, or `failed` with `error`. Needs the `publish` ability; the API key that wrote the draft cannot approve it (`403`, `code: self_approval`). A draft is sent at most once: approving again returns `409`. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_inbox_reply_draft201_response import CreateInboxReplyDraft201Response
from postboost.models.inbox_reply_draft_approve import InboxReplyDraftApprove
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.InboxApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    draft_id = 'draft_id_example' # str | The draft `id`.
    inbox_reply_draft_approve = postboost.InboxReplyDraftApprove() # InboxReplyDraftApprove |  (optional)

    try:
        # Approve and send a reply draft
        api_response = api_instance.approve_inbox_reply_draft(workspace_uuid, draft_id, inbox_reply_draft_approve=inbox_reply_draft_approve)
        print("The response of InboxApi->approve_inbox_reply_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->approve_inbox_reply_draft: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **draft_id** | **str**| The draft &#x60;id&#x60;. | 
 **inbox_reply_draft_approve** | [**InboxReplyDraftApprove**](InboxReplyDraftApprove.md)|  | [optional] 

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The reviewed draft |  -  |
**401** |  |  -  |
**403** | Not allowed: not a workspace admin or member, a scoped key without the &#x60;publish&#x60; ability (&#x60;code: insufficient_scope&#x60;), or the key that wrote the draft (&#x60;code: self_approval&#x60;).  |  -  |
**404** |  |  -  |
**409** | The draft was already reviewed. |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_inbox_reply_draft**
> CreateInboxReplyDraft201Response create_inbox_reply_draft(workspace_uuid, conversation_id, inbox_reply_draft_input)

Draft a reply

Proposes a reply. Nothing is posted: a person approves the draft in the app (Reply drafts page) or another API key with the `publish` ability approves it. `in_reply_to` defaults to the latest incoming message. The body limit depends on the network (Bluesky 300, Mastodon 500, LinkedIn 1250, Google 4000). Needs the `write` ability. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_inbox_reply_draft201_response import CreateInboxReplyDraft201Response
from postboost.models.inbox_reply_draft_input import InboxReplyDraftInput
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.InboxApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    conversation_id = 'conversation_id_example' # str | The conversation `id`.
    inbox_reply_draft_input = postboost.InboxReplyDraftInput() # InboxReplyDraftInput | 

    try:
        # Draft a reply
        api_response = api_instance.create_inbox_reply_draft(workspace_uuid, conversation_id, inbox_reply_draft_input)
        print("The response of InboxApi->create_inbox_reply_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->create_inbox_reply_draft: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **conversation_id** | **str**| The conversation &#x60;id&#x60;. | 
 **inbox_reply_draft_input** | [**InboxReplyDraftInput**](InboxReplyDraftInput.md)|  | 

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The pending draft |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_inbox_reply_draft**
> delete_inbox_reply_draft(workspace_uuid, draft_id)

Withdraw a reply draft

Deletes a pending draft. `409` once it was reviewed. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.InboxApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    draft_id = 'draft_id_example' # str | The draft `id`.

    try:
        # Withdraw a reply draft
        api_instance.delete_inbox_reply_draft(workspace_uuid, draft_id)
    except Exception as e:
        print("Exception when calling InboxApi->delete_inbox_reply_draft: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **draft_id** | **str**| The draft &#x60;id&#x60;. | 

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Deleted |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**409** | The draft was already reviewed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_inbox_conversation**
> GetInboxConversation200Response get_inbox_conversation(workspace_uuid, conversation_id)

Get an inbox conversation

The conversation with its 50 most recent messages, oldest first. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_inbox_conversation200_response import GetInboxConversation200Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.InboxApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    conversation_id = 'conversation_id_example' # str | The conversation `id`.

    try:
        # Get an inbox conversation
        api_response = api_instance.get_inbox_conversation(workspace_uuid, conversation_id)
        print("The response of InboxApi->get_inbox_conversation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->get_inbox_conversation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **conversation_id** | **str**| The conversation &#x60;id&#x60;. | 

### Return type

[**GetInboxConversation200Response**](GetInboxConversation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The conversation |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_inbox_reply_draft**
> CreateInboxReplyDraft201Response get_inbox_reply_draft(workspace_uuid, draft_id)

Get a reply draft

One draft. Poll it to see whether it was approved and sent. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_inbox_reply_draft201_response import CreateInboxReplyDraft201Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.InboxApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    draft_id = 'draft_id_example' # str | The draft `id`.

    try:
        # Get a reply draft
        api_response = api_instance.get_inbox_reply_draft(workspace_uuid, draft_id)
        print("The response of InboxApi->get_inbox_reply_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->get_inbox_reply_draft: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **draft_id** | **str**| The draft &#x60;id&#x60;. | 

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The draft |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_inbox_conversations**
> ListInboxConversations200Response list_inbox_conversations(workspace_uuid, status=status, account_id=account_id, provider=provider, unread=unread, sentiment=sentiment, ai_label=ai_label, since=since, page=page)

List inbox conversations

Comments, mentions and reviews on your accounts, most recent activity first, 25 per page. Available for Bluesky, Mastodon, LinkedIn Pages and Google Business Profile. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_inbox_conversations200_response import ListInboxConversations200Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.InboxApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    status = 'status_example' # str | Conversation status. (optional)
    account_id = 56 # int | Account `id`. (optional)
    provider = 'provider_example' # str | Network, for example `bluesky`. (optional)
    unread = True # bool | Only unread (`true`) or read (`false`) conversations. (optional)
    sentiment = 'sentiment_example' # str | AI sentiment. (optional)
    ai_label = 'ai_label_example' # str | AI label. (optional)
    since = '2013-10-20T19:20:30+01:00' # datetime | Only conversations with activity at or after this time. (optional)
    page = 1 # int | Page number. (optional) (default to 1)

    try:
        # List inbox conversations
        api_response = api_instance.list_inbox_conversations(workspace_uuid, status=status, account_id=account_id, provider=provider, unread=unread, sentiment=sentiment, ai_label=ai_label, since=since, page=page)
        print("The response of InboxApi->list_inbox_conversations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->list_inbox_conversations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **status** | **str**| Conversation status. | [optional] 
 **account_id** | **int**| Account &#x60;id&#x60;. | [optional] 
 **provider** | **str**| Network, for example &#x60;bluesky&#x60;. | [optional] 
 **unread** | **bool**| Only unread (&#x60;true&#x60;) or read (&#x60;false&#x60;) conversations. | [optional] 
 **sentiment** | **str**| AI sentiment. | [optional] 
 **ai_label** | **str**| AI label. | [optional] 
 **since** | **datetime**| Only conversations with activity at or after this time. | [optional] 
 **page** | **int**| Page number. | [optional] [default to 1]

### Return type

[**ListInboxConversations200Response**](ListInboxConversations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Conversations |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_inbox_reply_drafts**
> ListInboxReplyDrafts200Response list_inbox_reply_drafts(workspace_uuid, status=status, conversation_id=conversation_id, page=page)

List reply drafts

Reply drafts, newest first, 25 per page. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_inbox_reply_drafts200_response import ListInboxReplyDrafts200Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.InboxApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    status = 'status_example' # str | Draft status. (optional)
    conversation_id = 'conversation_id_example' # str | Only drafts for this conversation `id`. (optional)
    page = 1 # int | Page number. (optional) (default to 1)

    try:
        # List reply drafts
        api_response = api_instance.list_inbox_reply_drafts(workspace_uuid, status=status, conversation_id=conversation_id, page=page)
        print("The response of InboxApi->list_inbox_reply_drafts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->list_inbox_reply_drafts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **status** | **str**| Draft status. | [optional] 
 **conversation_id** | **str**| Only drafts for this conversation &#x60;id&#x60;. | [optional] 
 **page** | **int**| Page number. | [optional] [default to 1]

### Return type

[**ListInboxReplyDrafts200Response**](ListInboxReplyDrafts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Drafts |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reject_inbox_reply_draft**
> CreateInboxReplyDraft201Response reject_inbox_reply_draft(workspace_uuid, draft_id)

Reject a reply draft

Rejects a pending draft; nothing is sent. Needs the `publish` ability. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_inbox_reply_draft201_response import CreateInboxReplyDraft201Response
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.InboxApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    draft_id = 'draft_id_example' # str | The draft `id`.

    try:
        # Reject a reply draft
        api_response = api_instance.reject_inbox_reply_draft(workspace_uuid, draft_id)
        print("The response of InboxApi->reject_inbox_reply_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->reject_inbox_reply_draft: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **draft_id** | **str**| The draft &#x60;id&#x60;. | 

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The rejected draft |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**409** | The draft was already reviewed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_inbox_conversation**
> GetInboxConversation200Response update_inbox_conversation(workspace_uuid, conversation_id, inbox_conversation_update)

Update an inbox conversation

Marks the conversation open or resolved, read or unread. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_inbox_conversation200_response import GetInboxConversation200Response
from postboost.models.inbox_conversation_update import InboxConversationUpdate
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.InboxApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    conversation_id = 'conversation_id_example' # str | The conversation `id`.
    inbox_conversation_update = postboost.InboxConversationUpdate() # InboxConversationUpdate | 

    try:
        # Update an inbox conversation
        api_response = api_instance.update_inbox_conversation(workspace_uuid, conversation_id, inbox_conversation_update)
        print("The response of InboxApi->update_inbox_conversation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->update_inbox_conversation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **conversation_id** | **str**| The conversation &#x60;id&#x60;. | 
 **inbox_conversation_update** | [**InboxConversationUpdate**](InboxConversationUpdate.md)|  | 

### Return type

[**GetInboxConversation200Response**](GetInboxConversation200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The conversation |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_inbox_reply_draft**
> CreateInboxReplyDraft201Response update_inbox_reply_draft(workspace_uuid, draft_id, inbox_reply_draft_edit)

Edit a reply draft

Changes the text of a pending draft. `409` once it was reviewed. Requires the inbox API to be enabled for the workspace (otherwise `404`). Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_inbox_reply_draft201_response import CreateInboxReplyDraft201Response
from postboost.models.inbox_reply_draft_edit import InboxReplyDraftEdit
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: bearerAuth
configuration = postboost.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.InboxApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    draft_id = 'draft_id_example' # str | The draft `id`.
    inbox_reply_draft_edit = postboost.InboxReplyDraftEdit() # InboxReplyDraftEdit | 

    try:
        # Edit a reply draft
        api_response = api_instance.update_inbox_reply_draft(workspace_uuid, draft_id, inbox_reply_draft_edit)
        print("The response of InboxApi->update_inbox_reply_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->update_inbox_reply_draft: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **draft_id** | **str**| The draft &#x60;id&#x60;. | 
 **inbox_reply_draft_edit** | [**InboxReplyDraftEdit**](InboxReplyDraftEdit.md)|  | 

### Return type

[**CreateInboxReplyDraft201Response**](CreateInboxReplyDraft201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The draft |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**409** | The draft was already reviewed. |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


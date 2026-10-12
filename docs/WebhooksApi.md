# postboost.WebhooksApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_webhook_subscription**](WebhooksApi.md#create_webhook_subscription) | **POST** /{workspaceUuid}/webhooks/subscriptions | Subscribe a webhook
[**delete_webhook_subscription**](WebhooksApi.md#delete_webhook_subscription) | **DELETE** /{workspaceUuid}/webhooks/subscriptions/{subscriptionUuid} | Unsubscribe a webhook
[**list_webhook_subscriptions**](WebhooksApi.md#list_webhook_subscriptions) | **GET** /{workspaceUuid}/webhooks/subscriptions | List webhook subscriptions


# **create_webhook_subscription**
> CreateWebhookSubscription201Response create_webhook_subscription(workspace_uuid, webhook_subscription_input)

Subscribe a webhook

Registers a callback URL for the given events, the way n8n, Zapier and Make instant triggers do. Deliveries are `POST` requests with a JSON body (see [Webhooks](/webhooks) for the payload), signed with the returned `secret` in `X-Signature` (HMAC-SHA256 of the raw body, hex encoded) and attempted up to 3 times. Only public `https://` URLs are accepted. The `secret` is in this response only. Workspace admins only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_webhook_subscription201_response import CreateWebhookSubscription201Response
from postboost.models.webhook_subscription_input import WebhookSubscriptionInput
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
    api_instance = postboost.WebhooksApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    webhook_subscription_input = {"callback_url":"https://n8n.example.com/webhook/7d1c0c2e/postboost","events":["post.published","post.publishing_failed"],"source":"n8n"} # WebhookSubscriptionInput | 

    try:
        # Subscribe a webhook
        api_response = api_instance.create_webhook_subscription(workspace_uuid, webhook_subscription_input)
        print("The response of WebhooksApi->create_webhook_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->create_webhook_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **webhook_subscription_input** | [**WebhookSubscriptionInput**](WebhookSubscriptionInput.md)|  | 

### Return type

[**CreateWebhookSubscription201Response**](CreateWebhookSubscription201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The subscription was created |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_webhook_subscription**
> object delete_webhook_subscription(workspace_uuid, subscription_uuid)

Unsubscribe a webhook

Deletes the webhook and stops its deliveries. Workspace admins only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.object import object
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
    api_instance = postboost.WebhooksApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    subscription_uuid = 'subscription_uuid_example' # str | UUID of the webhook subscription.

    try:
        # Unsubscribe a webhook
        api_response = api_instance.delete_webhook_subscription(workspace_uuid, subscription_uuid)
        print("The response of WebhooksApi->delete_webhook_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->delete_webhook_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **subscription_uuid** | **str**| UUID of the webhook subscription. | 

### Return type

**object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_webhook_subscriptions**
> ListWebhookSubscriptions200Response list_webhook_subscriptions(workspace_uuid)

List webhook subscriptions

The workspace's webhooks, newest first: subscriptions created through this API and the ones added in **Settings → Webhooks**. Secrets are never returned here. Workspace admins only; needs the `webhooks` plan capability and, for scoped keys, the `webhooks` ability. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_webhook_subscriptions200_response import ListWebhookSubscriptions200Response
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
    api_instance = postboost.WebhooksApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # List webhook subscriptions
        api_response = api_instance.list_webhook_subscriptions(workspace_uuid)
        print("The response of WebhooksApi->list_webhook_subscriptions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->list_webhook_subscriptions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**ListWebhookSubscriptions200Response**](ListWebhookSubscriptions200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The workspace&#39;s webhooks |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


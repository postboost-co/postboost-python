# postboost.SubscriptionsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_generic_subscription**](SubscriptionsApi.md#add_generic_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/generic | Add generic subscription
[**cancel_subscription**](SubscriptionsApi.md#cancel_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/cancel | Cancel subscription
[**change_subscription_plan**](SubscriptionsApi.md#change_subscription_plan) | **PUT** /panel/workspaces/{workspaceUuid}/subscription/change-plan | Change subscription plan
[**checkout_subscription**](SubscriptionsApi.md#checkout_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/new | New subscription checkout
[**create_subscription**](SubscriptionsApi.md#create_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription | Create subscription
[**delete_subscription**](SubscriptionsApi.md#delete_subscription) | **DELETE** /panel/workspaces/{workspaceUuid}/subscription | Delete subscription
[**get_subscription**](SubscriptionsApi.md#get_subscription) | **GET** /panel/workspaces/{workspaceUuid}/subscription | Get subscription
[**remove_generic_subscription**](SubscriptionsApi.md#remove_generic_subscription) | **DELETE** /panel/workspaces/{workspaceUuid}/subscription/generic | Remove generic subscription
[**resume_subscription**](SubscriptionsApi.md#resume_subscription) | **POST** /panel/workspaces/{workspaceUuid}/subscription/resume | Resume subscription
[**update_subscription**](SubscriptionsApi.md#update_subscription) | **PUT** /panel/workspaces/{workspaceUuid}/subscription | Update subscription


# **add_generic_subscription**
> object add_generic_subscription(workspace_uuid, add_generic_subscription_request)

Add generic subscription

Assigns a non-Stripe (generic) subscription plan to the workspace, optionally granting a trial period. Used for AppSumo-style lifetime deals. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.add_generic_subscription_request import AddGenericSubscriptionRequest
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
    api_instance = postboost.SubscriptionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    add_generic_subscription_request = postboost.AddGenericSubscriptionRequest() # AddGenericSubscriptionRequest | 

    try:
        # Add generic subscription
        api_response = api_instance.add_generic_subscription(workspace_uuid, add_generic_subscription_request)
        print("The response of SubscriptionsApi->add_generic_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->add_generic_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **add_generic_subscription_request** | [**AddGenericSubscriptionRequest**](AddGenericSubscriptionRequest.md)|  | 

### Return type

**object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **cancel_subscription**
> object cancel_subscription(workspace_uuid)

Cancel subscription

Cancels the workspace's Stripe subscription at the end of the current billing period. Admin only.

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
    api_instance = postboost.SubscriptionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # Cancel subscription
        api_response = api_instance.cancel_subscription(workspace_uuid)
        print("The response of SubscriptionsApi->cancel_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->cancel_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **change_subscription_plan**
> object change_subscription_plan(workspace_uuid, change_subscription_plan_request)

Change subscription plan

Switches the workspace to a different Stripe plan. Optionally prorates the change and bills immediately. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.change_subscription_plan_request import ChangeSubscriptionPlanRequest
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
    api_instance = postboost.SubscriptionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    change_subscription_plan_request = postboost.ChangeSubscriptionPlanRequest() # ChangeSubscriptionPlanRequest | 

    try:
        # Change subscription plan
        api_response = api_instance.change_subscription_plan(workspace_uuid, change_subscription_plan_request)
        print("The response of SubscriptionsApi->change_subscription_plan:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->change_subscription_plan: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **change_subscription_plan_request** | [**ChangeSubscriptionPlanRequest**](ChangeSubscriptionPlanRequest.md)|  | 

### Return type

**object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **checkout_subscription**
> CheckoutSubscription200Response checkout_subscription(workspace_uuid, checkout_subscription_request)

New subscription checkout

Returns a Stripe Checkout URL for a new subscription.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.checkout_subscription200_response import CheckoutSubscription200Response
from postboost.models.checkout_subscription_request import CheckoutSubscriptionRequest
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
    api_instance = postboost.SubscriptionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    checkout_subscription_request = postboost.CheckoutSubscriptionRequest() # CheckoutSubscriptionRequest | 

    try:
        # New subscription checkout
        api_response = api_instance.checkout_subscription(workspace_uuid, checkout_subscription_request)
        print("The response of SubscriptionsApi->checkout_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->checkout_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **checkout_subscription_request** | [**CheckoutSubscriptionRequest**](CheckoutSubscriptionRequest.md)|  | 

### Return type

[**CheckoutSubscription200Response**](CheckoutSubscription200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Checkout URL |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_subscription**
> object create_subscription(workspace_uuid, subscription_input)

Create subscription

Manually creates a subscription record for the workspace (for external billing integrations). Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.subscription_input import SubscriptionInput
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
    api_instance = postboost.SubscriptionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    subscription_input = postboost.SubscriptionInput() # SubscriptionInput | 

    try:
        # Create subscription
        api_response = api_instance.create_subscription(workspace_uuid, subscription_input)
        print("The response of SubscriptionsApi->create_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->create_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **subscription_input** | [**SubscriptionInput**](SubscriptionInput.md)|  | 

### Return type

**object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_subscription**
> object delete_subscription(workspace_uuid)

Delete subscription

Removes the subscription record from the workspace. Admin only.

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
    api_instance = postboost.SubscriptionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # Delete subscription
        api_response = api_instance.delete_subscription(workspace_uuid)
        print("The response of SubscriptionsApi->delete_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->delete_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_subscription**
> Subscription get_subscription(workspace_uuid)

Get subscription

Returns the active subscription for the workspace, or `null` if none exists. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.subscription import Subscription
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
    api_instance = postboost.SubscriptionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # Get subscription
        api_response = api_instance.get_subscription(workspace_uuid)
        print("The response of SubscriptionsApi->get_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->get_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**Subscription**](Subscription.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Subscription details or null |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_generic_subscription**
> object remove_generic_subscription(workspace_uuid)

Remove generic subscription

Removes the generic (non-Stripe) subscription from the workspace. Admin only.

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
    api_instance = postboost.SubscriptionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # Remove generic subscription
        api_response = api_instance.remove_generic_subscription(workspace_uuid)
        print("The response of SubscriptionsApi->remove_generic_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->remove_generic_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **resume_subscription**
> object resume_subscription(workspace_uuid)

Resume subscription

Resumes a previously canceled subscription before it expires. Admin only.

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
    api_instance = postboost.SubscriptionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # Resume subscription
        api_response = api_instance.resume_subscription(workspace_uuid)
        print("The response of SubscriptionsApi->resume_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->resume_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_subscription**
> object update_subscription(workspace_uuid, subscription_update_input)

Update subscription

Updates the plan ID, status, or trial/pause dates of an existing subscription. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.subscription_update_input import SubscriptionUpdateInput
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
    api_instance = postboost.SubscriptionsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    subscription_update_input = postboost.SubscriptionUpdateInput() # SubscriptionUpdateInput | 

    try:
        # Update subscription
        api_response = api_instance.update_subscription(workspace_uuid, subscription_update_input)
        print("The response of SubscriptionsApi->update_subscription:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SubscriptionsApi->update_subscription: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **subscription_update_input** | [**SubscriptionUpdateInput**](SubscriptionUpdateInput.md)|  | 

### Return type

**object**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


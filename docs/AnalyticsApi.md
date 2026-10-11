# postboost.AnalyticsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_account_analytics**](AnalyticsApi.md#get_account_analytics) | **GET** /{workspaceUuid}/analytics/accounts/{accountUuid} | Get account analytics
[**get_analytics_summary**](AnalyticsApi.md#get_analytics_summary) | **GET** /{workspaceUuid}/analytics | Get analytics summary
[**get_best_posting_times**](AnalyticsApi.md#get_best_posting_times) | **GET** /{workspaceUuid}/analytics/best-times | Get best posting times
[**get_post_analytics_0**](AnalyticsApi.md#get_post_analytics_0) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics
[**get_posting_times**](AnalyticsApi.md#get_posting_times) | **GET** /{workspaceUuid}/analytics/posting-times | Get posting times heatmap


# **get_account_analytics**
> AccountAnalytics get_account_analytics(workspace_uuid, account_uuid, period=period, date_from=date_from, date_to=date_to, type=type, page=page, per_page=per_page, sort_by=sort_by, sort_dir=sort_dir)

Get account analytics

Analytics for one account. `type` selects one of the tabs the account supports (listed in `tabs` of the response); returns `422` when the account does not support analytics.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.account_analytics import AccountAnalytics
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
    api_instance = postboost.AnalyticsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    account_uuid = 'account_uuid_example' # str | UUID of the social media account.
    period = this_month # str | Preset reporting period. Ignored when `date_from` and `date_to` are given. (optional) (default to this_month)
    date_from = '2013-10-20' # date | Start of a custom range (Y-m-d). Required with `date_to`; the range may span at most 366 days. (optional)
    date_to = '2013-10-20' # date | End of a custom range (Y-m-d). Required with `date_from`; must not be before it. (optional)
    type = 'type_example' # str | Analytics tab. Defaults to the account's default tab. (optional)
    page = 1 # int | Page for list-style tabs (for example per-post metrics). (optional) (default to 1)
    per_page = 56 # int |  (optional)
    sort_by = 'sort_by_example' # str |  (optional)
    sort_dir = desc # str |  (optional) (default to desc)

    try:
        # Get account analytics
        api_response = api_instance.get_account_analytics(workspace_uuid, account_uuid, period=period, date_from=date_from, date_to=date_to, type=type, page=page, per_page=per_page, sort_by=sort_by, sort_dir=sort_dir)
        print("The response of AnalyticsApi->get_account_analytics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalyticsApi->get_account_analytics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **account_uuid** | **str**| UUID of the social media account. | 
 **period** | **str**| Preset reporting period. Ignored when &#x60;date_from&#x60; and &#x60;date_to&#x60; are given. | [optional] [default to this_month]
 **date_from** | **date**| Start of a custom range (Y-m-d). Required with &#x60;date_to&#x60;; the range may span at most 366 days. | [optional] 
 **date_to** | **date**| End of a custom range (Y-m-d). Required with &#x60;date_from&#x60;; must not be before it. | [optional] 
 **type** | **str**| Analytics tab. Defaults to the account&#39;s default tab. | [optional] 
 **page** | **int**| Page for list-style tabs (for example per-post metrics). | [optional] [default to 1]
 **per_page** | **int**|  | [optional] 
 **sort_by** | **str**|  | [optional] 
 **sort_dir** | **str**|  | [optional] [default to desc]

### Return type

[**AccountAnalytics**](AccountAnalytics.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Account analytics |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_analytics_summary**
> AnalyticsSummary get_analytics_summary(workspace_uuid, period=period, date_from=date_from, date_to=date_to)

Get analytics summary

Cross-platform summary (followers, growth, posts, leaderboard, posting streak) over every account that supports analytics, for a preset period or a custom date range.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.analytics_summary import AnalyticsSummary
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
    api_instance = postboost.AnalyticsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    period = this_month # str | Preset reporting period. Ignored when `date_from` and `date_to` are given. (optional) (default to this_month)
    date_from = '2013-10-20' # date | Start of a custom range (Y-m-d). Required with `date_to`; the range may span at most 366 days. (optional)
    date_to = '2013-10-20' # date | End of a custom range (Y-m-d). Required with `date_from`; must not be before it. (optional)

    try:
        # Get analytics summary
        api_response = api_instance.get_analytics_summary(workspace_uuid, period=period, date_from=date_from, date_to=date_to)
        print("The response of AnalyticsApi->get_analytics_summary:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalyticsApi->get_analytics_summary: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **period** | **str**| Preset reporting period. Ignored when &#x60;date_from&#x60; and &#x60;date_to&#x60; are given. | [optional] [default to this_month]
 **date_from** | **date**| Start of a custom range (Y-m-d). Required with &#x60;date_to&#x60;; the range may span at most 366 days. | [optional] 
 **date_to** | **date**| End of a custom range (Y-m-d). Required with &#x60;date_from&#x60;; must not be before it. | [optional] 

### Return type

[**AnalyticsSummary**](AnalyticsSummary.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Analytics summary |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_best_posting_times**
> BestPostingTimes get_best_posting_times(workspace_uuid, accounts=accounts, var_from=var_from, timezone=timezone)

Get best posting times

The next recommended date and time per account, on or after `from` (never in the past), within the next 14 days.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.best_posting_times import BestPostingTimes
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
    api_instance = postboost.AnalyticsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    accounts = ['accounts_example'] # List[str] | Account UUIDs. Defaults to every account in the workspace. (optional)
    var_from = '2013-10-20' # date | Earliest date to recommend (Y-m-d). Defaults to now. (optional)
    timezone = 'timezone_example' # str | Timezone for `from` and the returned times. Defaults to the workspace timezone. (optional)

    try:
        # Get best posting times
        api_response = api_instance.get_best_posting_times(workspace_uuid, accounts=accounts, var_from=var_from, timezone=timezone)
        print("The response of AnalyticsApi->get_best_posting_times:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalyticsApi->get_best_posting_times: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **accounts** | [**List[str]**](str.md)| Account UUIDs. Defaults to every account in the workspace. | [optional] 
 **var_from** | **date**| Earliest date to recommend (Y-m-d). Defaults to now. | [optional] 
 **timezone** | **str**| Timezone for &#x60;from&#x60; and the returned times. Defaults to the workspace timezone. | [optional] 

### Return type

[**BestPostingTimes**](BestPostingTimes.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Best posting times |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_post_analytics_0**
> PostAnalytics get_post_analytics_0(workspace_uuid, post_uuid)

Get post analytics

Engagement metrics for a published post across its accounts (also works for trashed posts), with totals, trends and the best-performing account.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.post_analytics import PostAnalytics
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
    api_instance = postboost.AnalyticsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.

    try:
        # Get post analytics
        api_response = api_instance.get_post_analytics_0(workspace_uuid, post_uuid)
        print("The response of AnalyticsApi->get_post_analytics_0:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalyticsApi->get_post_analytics_0: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 

### Return type

[**PostAnalytics**](PostAnalytics.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Post analytics |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_posting_times**
> PostingTimes get_posting_times(workspace_uuid, accounts=accounts, timezone=timezone)

Get posting times heatmap

Engagement scores per weekday and hour, merged across the given accounts (all accounts when none is given), in the requested timezone. Also returns up to three recommended slots.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.posting_times import PostingTimes
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
    api_instance = postboost.AnalyticsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    accounts = ['accounts_example'] # List[str] | Account UUIDs. Defaults to every account in the workspace. (optional)
    timezone = 'Europe/Istanbul' # str | Timezone the grid is expressed in. Defaults to the workspace timezone. (optional)

    try:
        # Get posting times heatmap
        api_response = api_instance.get_posting_times(workspace_uuid, accounts=accounts, timezone=timezone)
        print("The response of AnalyticsApi->get_posting_times:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalyticsApi->get_posting_times: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **accounts** | [**List[str]**](str.md)| Account UUIDs. Defaults to every account in the workspace. | [optional] 
 **timezone** | **str**| Timezone the grid is expressed in. Defaults to the workspace timezone. | [optional] 

### Return type

[**PostingTimes**](PostingTimes.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Posting times |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


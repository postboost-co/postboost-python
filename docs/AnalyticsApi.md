# postboost.AnalyticsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_report_export**](AnalyticsApi.md#create_report_export) | **POST** /{workspaceUuid}/reports/exports | Create a report export
[**download_report_export**](AnalyticsApi.md#download_report_export) | **GET** /{workspaceUuid}/reports/exports/{exportUuid}/download | Download a report file
[**get_account_analytics**](AnalyticsApi.md#get_account_analytics) | **GET** /{workspaceUuid}/analytics/accounts/{accountUuid} | Get account analytics
[**get_analytics_summary**](AnalyticsApi.md#get_analytics_summary) | **GET** /{workspaceUuid}/analytics | Get analytics summary
[**get_best_posting_times**](AnalyticsApi.md#get_best_posting_times) | **GET** /{workspaceUuid}/analytics/best-times | Get best posting times
[**get_post_analytics_0**](AnalyticsApi.md#get_post_analytics_0) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics
[**get_posting_times**](AnalyticsApi.md#get_posting_times) | **GET** /{workspaceUuid}/analytics/posting-times | Get posting times heatmap
[**get_report_branding**](AnalyticsApi.md#get_report_branding) | **GET** /{workspaceUuid}/report-branding | Get the report branding
[**get_report_export**](AnalyticsApi.md#get_report_export) | **GET** /{workspaceUuid}/reports/exports/{exportUuid} | Get a report export
[**list_report_exports**](AnalyticsApi.md#list_report_exports) | **GET** /{workspaceUuid}/reports/exports | List report exports
[**update_report_branding**](AnalyticsApi.md#update_report_branding) | **PUT** /{workspaceUuid}/report-branding | Update the report branding
[**upload_report_branding_logo**](AnalyticsApi.md#upload_report_branding_logo) | **POST** /{workspaceUuid}/report-branding/logo | Upload the report logo


# **create_report_export**
> CreateReportExport201Response create_report_export(workspace_uuid, report_export_input)

Create a report export

Generates a report for a period (default `last_month`) or a custom `date_from`/`date_to` range: a branded PDF (summary, accounts, top 10 posts; the header uses the report branding) or a CSV with one row per published post and account (`dataset: posts`, default) or per account (`dataset: accounts`). CSV files are UTF-8 with a byte order mark. At most 500 posts per report. The file is ready when the call returns; fetch it from `download_url` with the same token. Admins and members only; 20 per minute. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_report_export201_response import CreateReportExport201Response
from postboost.models.report_export_input import ReportExportInput
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
    report_export_input = {"format":"pdf","period":"last_month"} # ReportExportInput | 

    try:
        # Create a report export
        api_response = api_instance.create_report_export(workspace_uuid, report_export_input)
        print("The response of AnalyticsApi->create_report_export:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalyticsApi->create_report_export: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **report_export_input** | [**ReportExportInput**](ReportExportInput.md)|  | 

### Return type

[**CreateReportExport201Response**](CreateReportExport201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The export (status &#x60;ready&#x60;, or &#x60;failed&#x60; with &#x60;error&#x60;) |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_report_export**
> bytearray download_report_export(workspace_uuid, export_uuid)

Download a report file

The PDF or CSV file. `410` once it expired (7 days) or if the export failed.

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
    api_instance = postboost.AnalyticsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    export_uuid = 'export_uuid_example' # str | UUID of the report export.

    try:
        # Download a report file
        api_response = api_instance.download_report_export(workspace_uuid, export_uuid)
        print("The response of AnalyticsApi->download_report_export:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalyticsApi->download_report_export: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **export_uuid** | **str**| UUID of the report export. | 

### Return type

**bytearray**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, text/csv, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The report file |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**410** | The file expired or the export failed. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

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

# **get_report_branding**
> GetReportBranding200Response get_report_branding(workspace_uuid)

Get the report branding

The white-label header of the workspace's PDF reports. Unset fields are `null`; the workspace name is used then.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_report_branding200_response import GetReportBranding200Response
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

    try:
        # Get the report branding
        api_response = api_instance.get_report_branding(workspace_uuid)
        print("The response of AnalyticsApi->get_report_branding:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalyticsApi->get_report_branding: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**GetReportBranding200Response**](GetReportBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The report branding |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_report_export**
> CreateReportExport201Response get_report_export(workspace_uuid, export_uuid)

Get a report export

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_report_export201_response import CreateReportExport201Response
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
    export_uuid = 'export_uuid_example' # str | UUID of the report export.

    try:
        # Get a report export
        api_response = api_instance.get_report_export(workspace_uuid, export_uuid)
        print("The response of AnalyticsApi->get_report_export:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalyticsApi->get_report_export: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **export_uuid** | **str**| UUID of the report export. | 

### Return type

[**CreateReportExport201Response**](CreateReportExport201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The export |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_report_exports**
> ListReportExports200Response list_report_exports(workspace_uuid)

List report exports

The workspace's latest 50 report exports, newest first. Files can be downloaded for 7 days.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_report_exports200_response import ListReportExports200Response
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

    try:
        # List report exports
        api_response = api_instance.list_report_exports(workspace_uuid)
        print("The response of AnalyticsApi->list_report_exports:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalyticsApi->list_report_exports: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**ListReportExports200Response**](ListReportExports200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Recent exports |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_report_branding**
> GetReportBranding200Response update_report_branding(workspace_uuid, report_branding_input)

Update the report branding

Name, colour and footer of PDF reports. Fields you leave out keep their value. Upload the logo with `uploadReportBrandingLogo`. Admins and members only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_report_branding200_response import GetReportBranding200Response
from postboost.models.report_branding_input import ReportBrandingInput
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
    report_branding_input = {"display_name":"Brightside Agency","primary_color":"#FF6600","footer_text":"Prepared by Brightside Agency","show_powered_by":false} # ReportBrandingInput | 

    try:
        # Update the report branding
        api_response = api_instance.update_report_branding(workspace_uuid, report_branding_input)
        print("The response of AnalyticsApi->update_report_branding:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalyticsApi->update_report_branding: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **report_branding_input** | [**ReportBrandingInput**](ReportBrandingInput.md)|  | 

### Return type

[**GetReportBranding200Response**](GetReportBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The saved branding |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_report_branding_logo**
> GetReportBranding200Response upload_report_branding_logo(workspace_uuid, logo)

Upload the report logo

PNG or JPEG, up to 1 MB (SVG is not accepted). Replaces the current logo. Admins and members only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_report_branding200_response import GetReportBranding200Response
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
    logo = None # bytearray | 

    try:
        # Upload the report logo
        api_response = api_instance.upload_report_branding_logo(workspace_uuid, logo)
        print("The response of AnalyticsApi->upload_report_branding_logo:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AnalyticsApi->upload_report_branding_logo: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **logo** | **bytearray**|  | 

### Return type

[**GetReportBranding200Response**](GetReportBranding200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The saved branding |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


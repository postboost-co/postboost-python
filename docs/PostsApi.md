# postboost.PostsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_post_to_queue**](PostsApi.md#add_post_to_queue) | **POST** /{workspaceUuid}/posts/add-to-queue/{postUuid} | Add post to queue
[**approve_post**](PostsApi.md#approve_post) | **POST** /{workspaceUuid}/posts/approve/{postUuid} | Approve post
[**create_post**](PostsApi.md#create_post) | **POST** /{workspaceUuid}/posts | Create post
[**create_recycling_rule**](PostsApi.md#create_recycling_rule) | **POST** /{workspaceUuid}/recycling-rules | Create a recycling rule
[**create_rss_feed**](PostsApi.md#create_rss_feed) | **POST** /{workspaceUuid}/rss-feeds | Add an RSS feed
[**delete_post**](PostsApi.md#delete_post) | **DELETE** /{workspaceUuid}/posts/{postUuid} | Delete post
[**delete_posts_bulk**](PostsApi.md#delete_posts_bulk) | **DELETE** /{workspaceUuid}/posts | Delete posts (bulk)
[**delete_recycling_rule**](PostsApi.md#delete_recycling_rule) | **DELETE** /{workspaceUuid}/recycling-rules/{ruleUuid} | Delete a recycling rule
[**delete_rss_feed**](PostsApi.md#delete_rss_feed) | **DELETE** /{workspaceUuid}/rss-feeds/{feedUuid} | Delete an RSS feed
[**get_post**](PostsApi.md#get_post) | **GET** /{workspaceUuid}/posts/{postUuid} | Get post
[**get_post_analytics**](PostsApi.md#get_post_analytics) | **GET** /{workspaceUuid}/posts/{postUuid}/analytics | Get post analytics
[**get_recycling_rule**](PostsApi.md#get_recycling_rule) | **GET** /{workspaceUuid}/recycling-rules/{ruleUuid} | Get a recycling rule
[**get_rss_feed**](PostsApi.md#get_rss_feed) | **GET** /{workspaceUuid}/rss-feeds/{feedUuid} | Get an RSS feed
[**list_posts**](PostsApi.md#list_posts) | **GET** /{workspaceUuid}/posts | List posts
[**list_recycling_rules**](PostsApi.md#list_recycling_rules) | **GET** /{workspaceUuid}/recycling-rules | List recycling rules
[**list_recycling_runs**](PostsApi.md#list_recycling_runs) | **GET** /{workspaceUuid}/recycling-rules/{ruleUuid}/runs | List a recycling rule&#39;s runs
[**list_rss_feeds**](PostsApi.md#list_rss_feeds) | **GET** /{workspaceUuid}/rss-feeds | List RSS feeds
[**poll_rss_feed**](PostsApi.md#poll_rss_feed) | **POST** /{workspaceUuid}/rss-feeds/{feedUuid}/poll | Check an RSS feed now
[**recycle_post**](PostsApi.md#recycle_post) | **POST** /{workspaceUuid}/posts/{postUuid}/recycle | Recycle a post on an interval
[**retry_post_account**](PostsApi.md#retry_post_account) | **POST** /{workspaceUuid}/posts/retry/{postUuid}/{accountUuid} | Retry publishing to one account
[**schedule_post**](PostsApi.md#schedule_post) | **POST** /{workspaceUuid}/posts/schedule/{postUuid} | Schedule post
[**update_post**](PostsApi.md#update_post) | **PUT** /{workspaceUuid}/posts/{postUuid} | Update post
[**update_recycling_rule**](PostsApi.md#update_recycling_rule) | **PUT** /{workspaceUuid}/recycling-rules/{ruleUuid} | Update, pause or resume a recycling rule
[**update_rss_feed**](PostsApi.md#update_rss_feed) | **PUT** /{workspaceUuid}/rss-feeds/{feedUuid} | Update, pause or resume an RSS feed
[**validate_post**](PostsApi.md#validate_post) | **POST** /{workspaceUuid}/posts/validate | Validate post (dry run)


# **add_post_to_queue**
> ScheduleResult add_post_to_queue(workspace_uuid, post_uuid, idempotency_key=idempotency_key, add_post_to_queue_request=add_post_to_queue_request)

Add post to queue

Add an existing post to the smart publishing queue. Each account of the post gets its own next free queue slot. Returns `422` when the post has no accounts, the posting schedule has no available times, or provider requirements are not met. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.add_post_to_queue_request import AddPostToQueueRequest
from postboost.models.schedule_result import ScheduleResult
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.
    idempotency_key = 'idempotency_key_example' # str | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  (optional)
    add_post_to_queue_request = postboost.AddPostToQueueRequest() # AddPostToQueueRequest |  (optional)

    try:
        # Add post to queue
        api_response = api_instance.add_post_to_queue(workspace_uuid, post_uuid, idempotency_key=idempotency_key, add_post_to_queue_request=add_post_to_queue_request)
        print("The response of PostsApi->add_post_to_queue:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->add_post_to_queue: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 
 **idempotency_key** | **str**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] 
 **add_post_to_queue_request** | [**AddPostToQueueRequest**](AddPostToQueueRequest.md)|  | [optional] 

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Queue confirmation |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **approve_post**
> ScheduleResult approve_post(workspace_uuid, post_uuid, idempotency_key=idempotency_key, approve_post_request=approve_post_request)

Approve post

Approve a post that is pending review. The approver may move the post with `date`/`time` (read in `timezone`) and set per-account times with `accounts_schedule`; without them the post keeps the time it was submitted with. Provider requirements are validated and reported as `422`. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.approve_post_request import ApprovePostRequest
from postboost.models.schedule_result import ScheduleResult
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.
    idempotency_key = 'idempotency_key_example' # str | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  (optional)
    approve_post_request = postboost.ApprovePostRequest() # ApprovePostRequest |  (optional)

    try:
        # Approve post
        api_response = api_instance.approve_post(workspace_uuid, post_uuid, idempotency_key=idempotency_key, approve_post_request=approve_post_request)
        print("The response of PostsApi->approve_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->approve_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 
 **idempotency_key** | **str**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] 
 **approve_post_request** | [**ApprovePostRequest**](ApprovePostRequest.md)|  | [optional] 

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Approval confirmation |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_post**
> Post create_post(workspace_uuid, post_input, idempotency_key=idempotency_key)

Create post

Create a new post. Use `schedule: true` with `date` and `time` to schedule, `schedule_now: true` to publish immediately, or `queue: true` to add to the smart publishing queue (each account gets its own queue slot).  `date`, `time` and `accounts_schedule` are read in `timezone` when given, otherwise in the workspace timezone. Use `accounts_schedule` to give individual accounts their own departure time.  Post bodies may reference mentions with `{{mention:<reference>}}` (see the Mentions endpoints). When the post is scheduled, provider requirements (for example a network that requires media) are validated up front and reported as `422`.  **First comment and threads.** A version's `content` is an ordered array. Item 0 is the post. Add a second item to publish a first comment on Facebook Page, Instagram and LinkedIn, or to continue a thread on X, Threads, Bluesky, Mastodon and Pixelfed:  ```json {   \"accounts\": [12],   \"schedule_now\": true,   \"versions\": [{     \"account_id\": 0,     \"is_original\": true,     \"content\": [       { \"body\": \"Our API 1.8 is live.\", \"media\": [345] },       { \"body\": \"Full changelog: https://postboost.co/docs/changelog/\" }     ]   }] } ```  The comment is posted right after the post goes live. If the comment fails, the post stays published and the account's entry on the post reports the error. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.post import Post
from postboost.models.post_input import PostInput
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_input = postboost.PostInput() # PostInput | 
    idempotency_key = 'idempotency_key_example' # str | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  (optional)

    try:
        # Create post
        api_response = api_instance.create_post(workspace_uuid, post_input, idempotency_key=idempotency_key)
        print("The response of PostsApi->create_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->create_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_input** | [**PostInput**](PostInput.md)|  | 
 **idempotency_key** | **str**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] 

### Return type

[**Post**](Post.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created post |  * Idempotent-Replayed -  <br>  |
**400** |  |  -  |
**401** |  |  -  |
**403** |  |  -  |
**409** |  |  -  |
**422** |  |  -  |
**429** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_recycling_rule**
> CreateRecyclingRule201Response create_recycling_rule(workspace_uuid, recycling_rule_input)

Create a recycling rule

Recycles one post (`post_uuid`) or a tag pool (`type: tag_pool` + `tag_uuid`) every `interval_days`. The first run is `start_at`, or one interval from now. Copies are never published immediately: `placement: queue` (default) takes each account's next free queue slot, `same_time` schedules at the source post's time of day, `draft` leaves a draft.  Copies pass the same guardrails as posts created through the API (duplicate guard, per-account daily caps, disconnected accounts, X monthly allowance). A refused copy is not created; the run is logged with the guard's code (see the runs endpoint). X accounts are left out of copies because X rejects repeated text. Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_recycling_rule201_response import CreateRecyclingRule201Response
from postboost.models.recycling_rule_input import RecyclingRuleInput
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    recycling_rule_input = {"post_uuid":"3f2b6c1e-8a4d-4f7e-9b2a-1c5d6e7f8a9b","interval_days":30,"max_runs":6,"placement":"queue"} # RecyclingRuleInput | 

    try:
        # Create a recycling rule
        api_response = api_instance.create_recycling_rule(workspace_uuid, recycling_rule_input)
        print("The response of PostsApi->create_recycling_rule:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->create_recycling_rule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **recycling_rule_input** | [**RecyclingRuleInput**](RecyclingRuleInput.md)|  | 

### Return type

[**CreateRecyclingRule201Response**](CreateRecyclingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The rule was created |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_rss_feed**
> CreateRssFeed201Response create_rss_feed(workspace_uuid, rss_feed_input)

Add an RSS feed

Checks the feed every 30 minutes and turns each item published after the feed was added into a post for `account_ids`: a draft (`mode: draft`, default) or a queued post (`mode: queue`). The text comes from `template` with `{title}`, `{link}` and `{summary}` placeholders. Each item becomes at most one post, at most `max_items_per_run` per check and 20 per workspace per day. Posts pass the same guardrails as API-created posts. Only public http(s) URLs are accepted. Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_rss_feed201_response import CreateRssFeed201Response
from postboost.models.rss_feed_input import RssFeedInput
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    rss_feed_input = {"url":"https://blog.example.com/feed","name":"Company blog","account_ids":[12,14],"mode":"draft","template":"New on the blog: {title} {link}"} # RssFeedInput | 

    try:
        # Add an RSS feed
        api_response = api_instance.create_rss_feed(workspace_uuid, rss_feed_input)
        print("The response of PostsApi->create_rss_feed:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->create_rss_feed: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **rss_feed_input** | [**RssFeedInput**](RssFeedInput.md)|  | 

### Return type

[**CreateRssFeed201Response**](CreateRssFeed201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The feed was added |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_post**
> DeleteResult delete_post(workspace_uuid, post_uuid, delete_post_request=delete_post_request)

Delete post

Deletes a post. Use `delete_mode` to control whether to also remove the published content from social platforms.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.delete_post_request import DeletePostRequest
from postboost.models.delete_result import DeleteResult
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.
    delete_post_request = postboost.DeletePostRequest() # DeletePostRequest |  (optional)

    try:
        # Delete post
        api_response = api_instance.delete_post(workspace_uuid, post_uuid, delete_post_request=delete_post_request)
        print("The response of PostsApi->delete_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->delete_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 
 **delete_post_request** | [**DeletePostRequest**](DeletePostRequest.md)|  | [optional] 

### Return type

[**DeleteResult**](DeleteResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Deletion result |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_posts_bulk**
> DeleteResult delete_posts_bulk(workspace_uuid, delete_posts_bulk_request)

Delete posts (bulk)

Delete multiple posts at once.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.delete_posts_bulk_request import DeletePostsBulkRequest
from postboost.models.delete_result import DeleteResult
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    delete_posts_bulk_request = postboost.DeletePostsBulkRequest() # DeletePostsBulkRequest | 

    try:
        # Delete posts (bulk)
        api_response = api_instance.delete_posts_bulk(workspace_uuid, delete_posts_bulk_request)
        print("The response of PostsApi->delete_posts_bulk:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->delete_posts_bulk: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **delete_posts_bulk_request** | [**DeletePostsBulkRequest**](DeletePostsBulkRequest.md)|  | 

### Return type

[**DeleteResult**](DeleteResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Deletion result |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_recycling_rule**
> object delete_recycling_rule(workspace_uuid, rule_uuid)

Delete a recycling rule

Deletes the rule and its run log. Copies it already created stay. Admins and members only.

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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    rule_uuid = 'rule_uuid_example' # str | UUID of the recycling rule.

    try:
        # Delete a recycling rule
        api_response = api_instance.delete_recycling_rule(workspace_uuid, rule_uuid)
        print("The response of PostsApi->delete_recycling_rule:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->delete_recycling_rule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **rule_uuid** | **str**| UUID of the recycling rule. | 

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

# **delete_rss_feed**
> object delete_rss_feed(workspace_uuid, feed_uuid)

Delete an RSS feed

Stops the feed. Posts it already created stay. Admins and members only.

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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    feed_uuid = 'feed_uuid_example' # str | UUID of the RSS feed.

    try:
        # Delete an RSS feed
        api_response = api_instance.delete_rss_feed(workspace_uuid, feed_uuid)
        print("The response of PostsApi->delete_rss_feed:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->delete_rss_feed: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **feed_uuid** | **str**| UUID of the RSS feed. | 

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

# **get_post**
> Post get_post(workspace_uuid, post_uuid)

Get post

Returns a single post with all its versions and associated accounts.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.post import Post
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.

    try:
        # Get post
        api_response = api_instance.get_post(workspace_uuid, post_uuid)
        print("The response of PostsApi->get_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->get_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 

### Return type

[**Post**](Post.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Post details |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_post_analytics**
> PostAnalytics get_post_analytics(workspace_uuid, post_uuid)

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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.

    try:
        # Get post analytics
        api_response = api_instance.get_post_analytics(workspace_uuid, post_uuid)
        print("The response of PostsApi->get_post_analytics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->get_post_analytics: %s\n" % e)
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

# **get_recycling_rule**
> CreateRecyclingRule201Response get_recycling_rule(workspace_uuid, rule_uuid)

Get a recycling rule

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_recycling_rule201_response import CreateRecyclingRule201Response
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    rule_uuid = 'rule_uuid_example' # str | UUID of the recycling rule.

    try:
        # Get a recycling rule
        api_response = api_instance.get_recycling_rule(workspace_uuid, rule_uuid)
        print("The response of PostsApi->get_recycling_rule:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->get_recycling_rule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **rule_uuid** | **str**| UUID of the recycling rule. | 

### Return type

[**CreateRecyclingRule201Response**](CreateRecyclingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The rule |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_rss_feed**
> CreateRssFeed201Response get_rss_feed(workspace_uuid, feed_uuid)

Get an RSS feed

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_rss_feed201_response import CreateRssFeed201Response
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    feed_uuid = 'feed_uuid_example' # str | UUID of the RSS feed.

    try:
        # Get an RSS feed
        api_response = api_instance.get_rss_feed(workspace_uuid, feed_uuid)
        print("The response of PostsApi->get_rss_feed:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->get_rss_feed: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **feed_uuid** | **str**| UUID of the RSS feed. | 

### Return type

[**CreateRssFeed201Response**](CreateRssFeed201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The feed |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_posts**
> ListPosts200Response list_posts(workspace_uuid, page=page)

List posts

Returns a paginated list of posts in the workspace.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_posts200_response import ListPosts200Response
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    page = 1 # int |  (optional) (default to 1)

    try:
        # List posts
        api_response = api_instance.list_posts(workspace_uuid, page=page)
        print("The response of PostsApi->list_posts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->list_posts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **page** | **int**|  | [optional] [default to 1]

### Return type

[**ListPosts200Response**](ListPosts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated list of posts |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_recycling_rules**
> ListRecyclingRules200Response list_recycling_rules(workspace_uuid)

List recycling rules

Evergreen recycling rules of the workspace, newest first. A rule copies a post (or the least recently recycled published post with a tag) every `interval_days` and places the copy in the queue. Copies are ordinary posts: they show in the calendar and the queue. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_recycling_rules200_response import ListRecyclingRules200Response
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # List recycling rules
        api_response = api_instance.list_recycling_rules(workspace_uuid)
        print("The response of PostsApi->list_recycling_rules:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->list_recycling_rules: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**ListRecyclingRules200Response**](ListRecyclingRules200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The workspace&#39;s recycling rules |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_recycling_runs**
> ListRecyclingRuns200Response list_recycling_runs(workspace_uuid, rule_uuid)

List a recycling rule's runs

The latest 100 runs of the rule, newest first: the copy each run created, or why it skipped (`source_unavailable`, `no_eligible_post`, `no_accounts`, `queue_full`, `x_skipped_identical_text`, or a guardrail code such as `duplicate_post` or `account_daily_cap_reached`). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_recycling_runs200_response import ListRecyclingRuns200Response
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    rule_uuid = 'rule_uuid_example' # str | UUID of the recycling rule.

    try:
        # List a recycling rule's runs
        api_response = api_instance.list_recycling_runs(workspace_uuid, rule_uuid)
        print("The response of PostsApi->list_recycling_runs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->list_recycling_runs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **rule_uuid** | **str**| UUID of the recycling rule. | 

### Return type

[**ListRecyclingRuns200Response**](ListRecyclingRuns200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The rule&#39;s runs |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_rss_feeds**
> ListRssFeeds200Response list_rss_feeds(workspace_uuid)

List RSS feeds

RSS and Atom feeds whose new items become posts, newest first.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_rss_feeds200_response import ListRssFeeds200Response
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # List RSS feeds
        api_response = api_instance.list_rss_feeds(workspace_uuid)
        print("The response of PostsApi->list_rss_feeds:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->list_rss_feeds: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**ListRssFeeds200Response**](ListRssFeeds200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The workspace&#39;s feeds |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **poll_rss_feed**
> PollRssFeed200Response poll_rss_feed(workspace_uuid, feed_uuid)

Check an RSS feed now

Reads the feed immediately instead of waiting for the next check. Limited to 6 calls per minute. Admins and members only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.poll_rss_feed200_response import PollRssFeed200Response
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    feed_uuid = 'feed_uuid_example' # str | UUID of the RSS feed.

    try:
        # Check an RSS feed now
        api_response = api_instance.poll_rss_feed(workspace_uuid, feed_uuid)
        print("The response of PostsApi->poll_rss_feed:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->poll_rss_feed: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **feed_uuid** | **str**| UUID of the RSS feed. | 

### Return type

[**PollRssFeed200Response**](PollRssFeed200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The feed was read |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** | The feed could not be read (HTTP error, not a feed, larger than 2 MB, private address). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **recycle_post**
> CreateRecyclingRule201Response recycle_post(workspace_uuid, post_uuid, recycling_rule_settings)

Recycle a post on an interval

Shortcut for creating a `post` recycling rule for this post. Same body as `createRecyclingRule` without `type`, `post_uuid` and `tag_uuid`. Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_recycling_rule201_response import CreateRecyclingRule201Response
from postboost.models.recycling_rule_settings import RecyclingRuleSettings
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.
    recycling_rule_settings = {"interval_days":14} # RecyclingRuleSettings | 

    try:
        # Recycle a post on an interval
        api_response = api_instance.recycle_post(workspace_uuid, post_uuid, recycling_rule_settings)
        print("The response of PostsApi->recycle_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->recycle_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 
 **recycling_rule_settings** | [**RecyclingRuleSettings**](RecyclingRuleSettings.md)|  | 

### Return type

[**CreateRecyclingRule201Response**](CreateRecyclingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The rule was created |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **retry_post_account**
> RetryPostAccountResult retry_post_account(workspace_uuid, post_uuid, account_uuid, idempotency_key=idempotency_key)

Retry publishing to one account

Re-publishes a post to a single account whose publishing failed. Returns `422` when the account is not on the post, the post is still publishing, or the account did not fail.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.retry_post_account_result import RetryPostAccountResult
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.
    account_uuid = 'account_uuid_example' # str | UUID of the social media account.
    idempotency_key = 'idempotency_key_example' # str | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  (optional)

    try:
        # Retry publishing to one account
        api_response = api_instance.retry_post_account(workspace_uuid, post_uuid, account_uuid, idempotency_key=idempotency_key)
        print("The response of PostsApi->retry_post_account:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->retry_post_account: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 
 **account_uuid** | **str**| UUID of the social media account. | 
 **idempotency_key** | **str**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] 

### Return type

[**RetryPostAccountResult**](RetryPostAccountResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Retry started |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **schedule_post**
> ScheduleResult schedule_post(workspace_uuid, post_uuid, schedule_post_request, idempotency_key=idempotency_key)

Schedule post

Schedule an existing post. Optionally move it with `date`/`time` (read in `timezone`) and give accounts their own times with `accounts_schedule`. Set `postNow: true` to publish immediately; publishing starts within the request and any per-account times are dropped. Provider requirements are validated and reported as `422`. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.schedule_post_request import SchedulePostRequest
from postboost.models.schedule_result import ScheduleResult
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.
    schedule_post_request = postboost.SchedulePostRequest() # SchedulePostRequest | 
    idempotency_key = 'idempotency_key_example' # str | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  (optional)

    try:
        # Schedule post
        api_response = api_instance.schedule_post(workspace_uuid, post_uuid, schedule_post_request, idempotency_key=idempotency_key)
        print("The response of PostsApi->schedule_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->schedule_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 
 **schedule_post_request** | [**SchedulePostRequest**](SchedulePostRequest.md)|  | 
 **idempotency_key** | **str**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] 

### Return type

[**ScheduleResult**](ScheduleResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Schedule confirmation |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_post**
> object update_post(workspace_uuid, post_uuid, post_input)

Update post

Replaces a post's versions, accounts, tags, and scheduling options. The post must not be in a published state. `timezone` is honoured: `date`, `time` and `accounts_schedule` are read in it. When the post stays scheduled, provider requirements are validated and reported as `422`. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.post_input import PostInput
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_uuid = 'post_uuid_example' # str | UUID of the post.
    post_input = postboost.PostInput() # PostInput | 

    try:
        # Update post
        api_response = api_instance.update_post(workspace_uuid, post_uuid, post_input)
        print("The response of PostsApi->update_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->update_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_uuid** | **str**| UUID of the post. | 
 **post_input** | [**PostInput**](PostInput.md)|  | 

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
**404** |  |  -  |
**409** |  |  -  |
**422** |  |  -  |
**429** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_recycling_rule**
> CreateRecyclingRule201Response update_recycling_rule(workspace_uuid, rule_uuid, recycling_rule_update)

Update, pause or resume a recycling rule

Changes the interval, limit, placement or accounts, or pauses (`active: false`) and resumes the rule. Fields you leave out keep their value. A rule that reached `max_runs` resumes only with a higher `max_runs`. Admins and members only. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_recycling_rule201_response import CreateRecyclingRule201Response
from postboost.models.recycling_rule_update import RecyclingRuleUpdate
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    rule_uuid = 'rule_uuid_example' # str | UUID of the recycling rule.
    recycling_rule_update = {"active":false} # RecyclingRuleUpdate | 

    try:
        # Update, pause or resume a recycling rule
        api_response = api_instance.update_recycling_rule(workspace_uuid, rule_uuid, recycling_rule_update)
        print("The response of PostsApi->update_recycling_rule:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->update_recycling_rule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **rule_uuid** | **str**| UUID of the recycling rule. | 
 **recycling_rule_update** | [**RecyclingRuleUpdate**](RecyclingRuleUpdate.md)|  | 

### Return type

[**CreateRecyclingRule201Response**](CreateRecyclingRule201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated rule |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_rss_feed**
> CreateRssFeed201Response update_rss_feed(workspace_uuid, feed_uuid, rss_feed_update)

Update, pause or resume an RSS feed

Fields you leave out keep their value. Resuming (`active: true`) clears the error backoff. Admins and members only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.create_rss_feed201_response import CreateRssFeed201Response
from postboost.models.rss_feed_update import RssFeedUpdate
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    feed_uuid = 'feed_uuid_example' # str | UUID of the RSS feed.
    rss_feed_update = {"active":false} # RssFeedUpdate | 

    try:
        # Update, pause or resume an RSS feed
        api_response = api_instance.update_rss_feed(workspace_uuid, feed_uuid, rss_feed_update)
        print("The response of PostsApi->update_rss_feed:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->update_rss_feed: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **feed_uuid** | **str**| UUID of the RSS feed. | 
 **rss_feed_update** | [**RssFeedUpdate**](RssFeedUpdate.md)|  | 

### Return type

[**CreateRssFeed201Response**](CreateRssFeed201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated feed |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validate_post**
> PreflightResult validate_post(workspace_uuid, post_input)

Validate post (dry run)

Runs everything create-post checks without creating anything: request validation, network requirements (text length, media count and type, links) for every given account, whether or not the post is scheduled, and the guardrails (duplicate content, daily caps, account health). Always answers `200`; read `valid`. Any workspace member, including viewers, may call it. Recommended agent loop: account health, validate, then create. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.post_input import PostInput
from postboost.models.preflight_result import PreflightResult
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
    api_instance = postboost.PostsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    post_input = postboost.PostInput() # PostInput | 

    try:
        # Validate post (dry run)
        api_response = api_instance.validate_post(workspace_uuid, post_input)
        print("The response of PostsApi->validate_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PostsApi->validate_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **post_input** | [**PostInput**](PostInput.md)|  | 

### Return type

[**PreflightResult**](PreflightResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Validation result |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


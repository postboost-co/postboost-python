# postboost.FreeToolsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**build_utm_url**](FreeToolsApi.md#build_utm_url) | **POST** /tools/utm-builder | Build a UTM-tagged campaign URL
[**calculate_crop**](FreeToolsApi.md#calculate_crop) | **POST** /tools/social-media-image-sizes/crop | Calculate the crop box that fits an image to a social media size
[**calculate_engagement_rate**](FreeToolsApi.md#calculate_engagement_rate) | **POST** /tools/engagement-rate-calculator | Calculate an engagement rate
[**check_post**](FreeToolsApi.md#check_post) | **POST** /tools/social-media-post-checker | Check a post against each network&#39;s publishing rules
[**clean_text**](FreeToolsApi.md#clean_text) | **POST** /tools/ai-text-cleaner | Clean AI-written text: dashes, quotes, invisible characters, markdown
[**count_characters**](FreeToolsApi.md#count_characters) | **POST** /tools/social-media-character-counter | Count characters as each network counts them
[**format_linked_in_post**](FreeToolsApi.md#format_linked_in_post) | **POST** /tools/linkedin-post-formatter | Format a LinkedIn post with bold, italic and lists
[**generate_caption**](FreeToolsApi.md#generate_caption) | **POST** /tools/instagram-caption-generator | Write three post captions for a topic with AI (needs a token, spends AI credits)
[**generate_fancy_text**](FreeToolsApi.md#generate_fancy_text) | **POST** /tools/fancy-text-generator | Convert text to fancy Unicode styles
[**generate_hashtags**](FreeToolsApi.md#generate_hashtags) | **POST** /tools/instagram-hashtag-generator | Generate hashtags for a post topic with AI (needs a token, spends AI credits)
[**get_best_times_to_post**](FreeToolsApi.md#get_best_times_to_post) | **GET** /tools/best-time-to-post | Get the best times to post per network from published studies, with sources
[**get_image_sizes**](FreeToolsApi.md#get_image_sizes) | **GET** /tools/social-media-image-sizes | Get social media image sizes per network, each with its source
[**list_free_tools**](FreeToolsApi.md#list_free_tools) | **GET** /tools | List the free tools
[**split_thread**](FreeToolsApi.md#split_thread) | **POST** /tools/x-thread-maker | Split long text into a thread


# **build_utm_url**
> FreeToolBuildUtmUrlResponse build_utm_url(free_tool_build_utm_url_request)

Build a UTM-tagged campaign URL

Build a UTM-tagged campaign URL. The same logic as the free web tool at https://postboost.co/tools/utm-builder. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_build_utm_url_request import FreeToolBuildUtmUrlRequest
from postboost.models.free_tool_build_utm_url_response import FreeToolBuildUtmUrlResponse
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)


# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.FreeToolsApi(api_client)
    free_tool_build_utm_url_request = {"url":"https://postboost.co/pricing?plan=pro#faq","utm_source":"linkedin","utm_medium":"social","utm_campaign":"q4 launch"} # FreeToolBuildUtmUrlRequest | 

    try:
        # Build a UTM-tagged campaign URL
        api_response = api_instance.build_utm_url(free_tool_build_utm_url_request)
        print("The response of FreeToolsApi->build_utm_url:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->build_utm_url: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_build_utm_url_request** | [**FreeToolBuildUtmUrlRequest**](FreeToolBuildUtmUrlRequest.md)|  | 

### Return type

[**FreeToolBuildUtmUrlResponse**](FreeToolBuildUtmUrlResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** |  |  -  |
**413** | The request body is larger than 128 KB. |  -  |
**422** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **calculate_crop**
> FreeToolCalculateCropResponse calculate_crop(free_tool_calculate_crop_request)

Calculate the crop box that fits an image to a social media size

Calculate the crop box that fits an image to a social media size. The same logic as the free web tool at https://postboost.co/tools/social-media-image-sizes. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_calculate_crop_request import FreeToolCalculateCropRequest
from postboost.models.free_tool_calculate_crop_response import FreeToolCalculateCropResponse
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)


# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.FreeToolsApi(api_client)
    free_tool_calculate_crop_request = {"width":4000,"height":3000,"network":"instagram","format":"feed-square"} # FreeToolCalculateCropRequest | 

    try:
        # Calculate the crop box that fits an image to a social media size
        api_response = api_instance.calculate_crop(free_tool_calculate_crop_request)
        print("The response of FreeToolsApi->calculate_crop:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->calculate_crop: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_calculate_crop_request** | [**FreeToolCalculateCropRequest**](FreeToolCalculateCropRequest.md)|  | 

### Return type

[**FreeToolCalculateCropResponse**](FreeToolCalculateCropResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** |  |  -  |
**413** | The request body is larger than 128 KB. |  -  |
**422** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **calculate_engagement_rate**
> FreeToolCalculateEngagementRateResponse calculate_engagement_rate(free_tool_calculate_engagement_rate_request)

Calculate an engagement rate

Calculate an engagement rate. The same logic as the free web tool at https://postboost.co/tools/engagement-rate-calculator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_calculate_engagement_rate_request import FreeToolCalculateEngagementRateRequest
from postboost.models.free_tool_calculate_engagement_rate_response import FreeToolCalculateEngagementRateResponse
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)


# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.FreeToolsApi(api_client)
    free_tool_calculate_engagement_rate_request = {"likes":120,"comments":30,"shares":10,"base":4000,"posts":2} # FreeToolCalculateEngagementRateRequest | 

    try:
        # Calculate an engagement rate
        api_response = api_instance.calculate_engagement_rate(free_tool_calculate_engagement_rate_request)
        print("The response of FreeToolsApi->calculate_engagement_rate:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->calculate_engagement_rate: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_calculate_engagement_rate_request** | [**FreeToolCalculateEngagementRateRequest**](FreeToolCalculateEngagementRateRequest.md)|  | 

### Return type

[**FreeToolCalculateEngagementRateResponse**](FreeToolCalculateEngagementRateResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** |  |  -  |
**413** | The request body is larger than 128 KB. |  -  |
**422** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **check_post**
> FreeToolCheckPostResponse check_post(free_tool_check_post_request)

Check a post against each network's publishing rules

Check a post against each network's publishing rules. The same logic as the free web tool at https://postboost.co/tools/social-media-post-checker. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_check_post_request import FreeToolCheckPostRequest
from postboost.models.free_tool_check_post_response import FreeToolCheckPostResponse
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)


# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.FreeToolsApi(api_client)
    free_tool_check_post_request = {"text":"Big news: https://postboost.co #launch","networks":["x","instagram"]} # FreeToolCheckPostRequest | 

    try:
        # Check a post against each network's publishing rules
        api_response = api_instance.check_post(free_tool_check_post_request)
        print("The response of FreeToolsApi->check_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->check_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_check_post_request** | [**FreeToolCheckPostRequest**](FreeToolCheckPostRequest.md)|  | 

### Return type

[**FreeToolCheckPostResponse**](FreeToolCheckPostResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** |  |  -  |
**413** | The request body is larger than 128 KB. |  -  |
**422** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clean_text**
> FreeToolCleanTextResponse clean_text(free_tool_clean_text_request)

Clean AI-written text: dashes, quotes, invisible characters, markdown

Clean AI-written text: dashes, quotes, invisible characters, markdown. The same logic as the free web tool at https://postboost.co/tools/ai-text-cleaner. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_clean_text_request import FreeToolCleanTextRequest
from postboost.models.free_tool_clean_text_response import FreeToolCleanTextResponse
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)


# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.FreeToolsApi(api_client)
    free_tool_clean_text_request = {"text":"Fast — reliable… and “simple”."} # FreeToolCleanTextRequest | 

    try:
        # Clean AI-written text: dashes, quotes, invisible characters, markdown
        api_response = api_instance.clean_text(free_tool_clean_text_request)
        print("The response of FreeToolsApi->clean_text:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->clean_text: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_clean_text_request** | [**FreeToolCleanTextRequest**](FreeToolCleanTextRequest.md)|  | 

### Return type

[**FreeToolCleanTextResponse**](FreeToolCleanTextResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** |  |  -  |
**413** | The request body is larger than 128 KB. |  -  |
**422** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **count_characters**
> FreeToolCountCharactersResponse count_characters(free_tool_count_characters_request)

Count characters as each network counts them

Count characters as each network counts them. The same logic as the free web tool at https://postboost.co/tools/social-media-character-counter. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_count_characters_request import FreeToolCountCharactersRequest
from postboost.models.free_tool_count_characters_response import FreeToolCountCharactersResponse
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)


# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.FreeToolsApi(api_client)
    free_tool_count_characters_request = {"text":"New post: https://postboost.co/tools","network":"x"} # FreeToolCountCharactersRequest | 

    try:
        # Count characters as each network counts them
        api_response = api_instance.count_characters(free_tool_count_characters_request)
        print("The response of FreeToolsApi->count_characters:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->count_characters: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_count_characters_request** | [**FreeToolCountCharactersRequest**](FreeToolCountCharactersRequest.md)|  | 

### Return type

[**FreeToolCountCharactersResponse**](FreeToolCountCharactersResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** |  |  -  |
**413** | The request body is larger than 128 KB. |  -  |
**422** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **format_linked_in_post**
> FreeToolFormatLinkedInPostResponse format_linked_in_post(free_tool_format_linked_in_post_request)

Format a LinkedIn post with bold, italic and lists

Format a LinkedIn post with bold, italic and lists. The same logic as the free web tool at https://postboost.co/tools/linkedin-post-formatter. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_format_linked_in_post_request import FreeToolFormatLinkedInPostRequest
from postboost.models.free_tool_format_linked_in_post_response import FreeToolFormatLinkedInPostResponse
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)


# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.FreeToolsApi(api_client)
    free_tool_format_linked_in_post_request = {"text":"Three tips\nPlan ahead\nReuse posts","list":"numbered"} # FreeToolFormatLinkedInPostRequest | 

    try:
        # Format a LinkedIn post with bold, italic and lists
        api_response = api_instance.format_linked_in_post(free_tool_format_linked_in_post_request)
        print("The response of FreeToolsApi->format_linked_in_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->format_linked_in_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_format_linked_in_post_request** | [**FreeToolFormatLinkedInPostRequest**](FreeToolFormatLinkedInPostRequest.md)|  | 

### Return type

[**FreeToolFormatLinkedInPostResponse**](FreeToolFormatLinkedInPostResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** |  |  -  |
**413** | The request body is larger than 128 KB. |  -  |
**422** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_caption**
> FreeToolGenerateCaptionResponse generate_caption(free_tool_generate_caption_request)

Write three post captions for a topic with AI (needs a token, spends AI credits)

Write three post captions for a topic with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/instagram-caption-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.free_tool_generate_caption_request import FreeToolGenerateCaptionRequest
from postboost.models.free_tool_generate_caption_response import FreeToolGenerateCaptionResponse
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
    api_instance = postboost.FreeToolsApi(api_client)
    free_tool_generate_caption_request = {"text":"Weekend sale on all candles","network":"instagram","tone":"playful","hashtags":true} # FreeToolGenerateCaptionRequest | 

    try:
        # Write three post captions for a topic with AI (needs a token, spends AI credits)
        api_response = api_instance.generate_caption(free_tool_generate_caption_request)
        print("The response of FreeToolsApi->generate_caption:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->generate_caption: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_generate_caption_request** | [**FreeToolGenerateCaptionRequest**](FreeToolGenerateCaptionRequest.md)|  | 

### Return type

[**FreeToolGenerateCaptionResponse**](FreeToolGenerateCaptionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** | No API token, or an invalid one. The body has &#x60;register_url&#x60; to create a free account. |  -  |
**403** | &#x60;workspace&#x60; is not a workspace you belong to, or your account has no workspace, or a scoped API key lacks the &#x60;ai&#x60; ability or is bound to another workspace (&#x60;code: insufficient_scope&#x60;). |  -  |
**413** | The request body is larger than 128 KB. |  -  |
**422** |  |  -  |
**429** | The workspace has no AI credits left this billing cycle (&#x60;code: ai_credits_exhausted&#x60;, &#x60;upgrade_url&#x60;), or the per-minute limit was reached. Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |
**502** | The AI provider failed or timed out. No credit was spent. |  -  |
**503** | AI tools are switched off right now. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_fancy_text**
> FreeToolGenerateFancyTextResponse generate_fancy_text(free_tool_generate_fancy_text_request)

Convert text to fancy Unicode styles

Convert text to fancy Unicode styles. The same logic as the free web tool at https://postboost.co/tools/fancy-text-generator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_generate_fancy_text_request import FreeToolGenerateFancyTextRequest
from postboost.models.free_tool_generate_fancy_text_response import FreeToolGenerateFancyTextResponse
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)


# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.FreeToolsApi(api_client)
    free_tool_generate_fancy_text_request = {"text":"Hello 123","style":"bold"} # FreeToolGenerateFancyTextRequest | 

    try:
        # Convert text to fancy Unicode styles
        api_response = api_instance.generate_fancy_text(free_tool_generate_fancy_text_request)
        print("The response of FreeToolsApi->generate_fancy_text:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->generate_fancy_text: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_generate_fancy_text_request** | [**FreeToolGenerateFancyTextRequest**](FreeToolGenerateFancyTextRequest.md)|  | 

### Return type

[**FreeToolGenerateFancyTextResponse**](FreeToolGenerateFancyTextResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** |  |  -  |
**413** | The request body is larger than 128 KB. |  -  |
**422** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_hashtags**
> FreeToolGenerateHashtagsResponse generate_hashtags(free_tool_generate_hashtags_request)

Generate hashtags for a post topic with AI (needs a token, spends AI credits)

Generate hashtags for a post topic with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/instagram-hashtag-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.free_tool_generate_hashtags_request import FreeToolGenerateHashtagsRequest
from postboost.models.free_tool_generate_hashtags_response import FreeToolGenerateHashtagsResponse
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
    api_instance = postboost.FreeToolsApi(api_client)
    free_tool_generate_hashtags_request = {"topic":"Morning routine for busy founders","network":"instagram"} # FreeToolGenerateHashtagsRequest | 

    try:
        # Generate hashtags for a post topic with AI (needs a token, spends AI credits)
        api_response = api_instance.generate_hashtags(free_tool_generate_hashtags_request)
        print("The response of FreeToolsApi->generate_hashtags:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->generate_hashtags: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_generate_hashtags_request** | [**FreeToolGenerateHashtagsRequest**](FreeToolGenerateHashtagsRequest.md)|  | 

### Return type

[**FreeToolGenerateHashtagsResponse**](FreeToolGenerateHashtagsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** | No API token, or an invalid one. The body has &#x60;register_url&#x60; to create a free account. |  -  |
**403** | &#x60;workspace&#x60; is not a workspace you belong to, or your account has no workspace, or a scoped API key lacks the &#x60;ai&#x60; ability or is bound to another workspace (&#x60;code: insufficient_scope&#x60;). |  -  |
**413** | The request body is larger than 128 KB. |  -  |
**422** |  |  -  |
**429** | The workspace has no AI credits left this billing cycle (&#x60;code: ai_credits_exhausted&#x60;, &#x60;upgrade_url&#x60;), or the per-minute limit was reached. Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |
**502** | The AI provider failed or timed out. No credit was spent. |  -  |
**503** | AI tools are switched off right now. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_best_times_to_post**
> FreeToolGetBestTimesToPostResponse get_best_times_to_post(network=network)

Get the best times to post per network from published studies, with sources

Get the best times to post per network from published studies, with sources. The same logic as the free web tool at https://postboost.co/tools/best-time-to-post. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_get_best_times_to_post_response import FreeToolGetBestTimesToPostResponse
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)


# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.FreeToolsApi(api_client)
    network = 'network_example' # str |  (optional)

    try:
        # Get the best times to post per network from published studies, with sources
        api_response = api_instance.get_best_times_to_post(network=network)
        print("The response of FreeToolsApi->get_best_times_to_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->get_best_times_to_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **network** | **str**|  | [optional] 

### Return type

[**FreeToolGetBestTimesToPostResponse**](FreeToolGetBestTimesToPostResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** |  |  -  |
**422** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_image_sizes**
> FreeToolGetImageSizesResponse get_image_sizes(network=network)

Get social media image sizes per network, each with its source

Get social media image sizes per network, each with its source. The same logic as the free web tool at https://postboost.co/tools/social-media-image-sizes. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_get_image_sizes_response import FreeToolGetImageSizesResponse
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)


# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.FreeToolsApi(api_client)
    network = 'network_example' # str |  (optional)

    try:
        # Get social media image sizes per network, each with its source
        api_response = api_instance.get_image_sizes(network=network)
        print("The response of FreeToolsApi->get_image_sizes:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->get_image_sizes: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **network** | **str**|  | [optional] 

### Return type

[**FreeToolGetImageSizesResponse**](FreeToolGetImageSizesResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** |  |  -  |
**422** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_free_tools**
> FreeToolList list_free_tools()

List the free tools

Every free tool the API serves, with its operationId and web page. No token needed.

### Example


```python
import postboost
from postboost.models.free_tool_list import FreeToolList
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)


# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.FreeToolsApi(api_client)

    try:
        # List the free tools
        api_response = api_instance.list_free_tools()
        print("The response of FreeToolsApi->list_free_tools:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->list_free_tools: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**FreeToolList**](FreeToolList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The free tools. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **split_thread**
> FreeToolSplitThreadResponse split_thread(free_tool_split_thread_request)

Split long text into a thread

Split long text into a thread. The same logic as the free web tool at https://postboost.co/tools/x-thread-maker. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_split_thread_request import FreeToolSplitThreadRequest
from postboost.models.free_tool_split_thread_response import FreeToolSplitThreadResponse
from postboost.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://postboost.co/app/api
# See configuration.py for a list of all supported configuration parameters.
configuration = postboost.Configuration(
    host = "https://postboost.co/app/api"
)


# Enter a context with an instance of the API client
with postboost.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = postboost.FreeToolsApi(api_client)
    free_tool_split_thread_request = {"text":"Short one.\n\nShort two.\n---\nSecond post.","numbering":true} # FreeToolSplitThreadRequest | 

    try:
        # Split long text into a thread
        api_response = api_instance.split_thread(free_tool_split_thread_request)
        print("The response of FreeToolsApi->split_thread:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->split_thread: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_split_thread_request** | [**FreeToolSplitThreadRequest**](FreeToolSplitThreadRequest.md)|  | 

### Return type

[**FreeToolSplitThreadResponse**](FreeToolSplitThreadResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** |  |  -  |
**413** | The request body is larger than 128 KB. |  -  |
**422** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


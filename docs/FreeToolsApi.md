# postboost.FreeToolsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**build_utm_url**](FreeToolsApi.md#build_utm_url) | **POST** /tools/utm-builder | Build a UTM-tagged campaign URL
[**calculate_aspect_ratio**](FreeToolsApi.md#calculate_aspect_ratio) | **POST** /tools/aspect-ratio-calculator | Calculate an aspect ratio, or the missing side of an image at a given ratio
[**calculate_crop**](FreeToolsApi.md#calculate_crop) | **POST** /tools/social-media-image-sizes/crop | Calculate the crop box that fits an image to a social media size
[**calculate_engagement_rate**](FreeToolsApi.md#calculate_engagement_rate) | **POST** /tools/engagement-rate-calculator | Calculate an engagement rate
[**calculate_social_roi**](FreeToolsApi.md#calculate_social_roi) | **POST** /tools/social-media-roi-calculator | Calculate social media ROI
[**check_link_preview**](FreeToolsApi.md#check_link_preview) | **POST** /tools/link-preview-checker | Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags)
[**check_post**](FreeToolsApi.md#check_post) | **POST** /tools/social-media-post-checker | Check a post against each network&#39;s publishing rules
[**check_youtube_thumbnail**](FreeToolsApi.md#check_youtube_thumbnail) | **POST** /tools/youtube-thumbnail-size-checker | Check a YouTube thumbnail&#39;s ratio, width, file size and format against YouTube&#39;s requirements
[**clean_text**](FreeToolsApi.md#clean_text) | **POST** /tools/ai-text-cleaner | Clean AI-written text: dashes, quotes, invisible characters, markdown
[**count_characters**](FreeToolsApi.md#count_characters) | **POST** /tools/social-media-character-counter | Count characters as each network counts them
[**format_instagram_caption**](FreeToolsApi.md#format_instagram_caption) | **POST** /tools/instagram-line-break-generator | Keep blank lines in an Instagram caption with spacer lines, and count it
[**format_linked_in_post**](FreeToolsApi.md#format_linked_in_post) | **POST** /tools/linkedin-post-formatter | Format a LinkedIn post with bold, italic and lists
[**generate_caption**](FreeToolsApi.md#generate_caption) | **POST** /tools/instagram-caption-generator | Write three post captions for a topic with AI (needs a token, spends AI credits)
[**generate_fancy_text**](FreeToolsApi.md#generate_fancy_text) | **POST** /tools/fancy-text-generator | Convert text to fancy Unicode styles
[**generate_hashtags**](FreeToolsApi.md#generate_hashtags) | **POST** /tools/instagram-hashtag-generator | Generate hashtags for a post topic with AI (needs a token, spends AI credits)
[**generate_hooks**](FreeToolsApi.md#generate_hooks) | **POST** /tools/hook-generator | Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits)
[**generate_qr_code**](FreeToolsApi.md#generate_qr_code) | **POST** /tools/qr-code-generator | Generate a QR code (SVG) for a link or text, with optional UTM tags
[**generate_social_posts_from_blog**](FreeToolsApi.md#generate_social_posts_from_blog) | **POST** /tools/blog-to-social-media | Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits)
[**get_best_times_to_post**](FreeToolsApi.md#get_best_times_to_post) | **GET** /tools/best-time-to-post | Get the best times to post per network from published studies, with sources
[**get_hook_templates**](FreeToolsApi.md#get_hook_templates) | **GET** /tools/hook-generator/library | Get free hook templates for social media posts, filtered by style and network
[**get_image_sizes**](FreeToolsApi.md#get_image_sizes) | **GET** /tools/social-media-image-sizes | Get social media image sizes per network, each with its source
[**get_video_specs**](FreeToolsApi.md#get_video_specs) | **GET** /tools/social-media-video-specs | Get social media video ratios, resolutions, lengths and file size limits per network, with sources
[**list_free_tools**](FreeToolsApi.md#list_free_tools) | **GET** /tools | List the free tools
[**plan_content_calendar**](FreeToolsApi.md#plan_content_calendar) | **POST** /tools/social-media-content-calendar-generator | Plan a social media content calendar and get it as CSV and ICS
[**preview_post**](FreeToolsApi.md#preview_post) | **POST** /tools/social-media-post-preview | Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook
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

# **calculate_aspect_ratio**
> FreeToolCalculateAspectRatioResponse calculate_aspect_ratio(free_tool_calculate_aspect_ratio_request)

Calculate an aspect ratio, or the missing side of an image at a given ratio

Calculate an aspect ratio, or the missing side of an image at a given ratio. The same logic as the free web tool at https://postboost.co/tools/aspect-ratio-calculator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_calculate_aspect_ratio_request import FreeToolCalculateAspectRatioRequest
from postboost.models.free_tool_calculate_aspect_ratio_response import FreeToolCalculateAspectRatioResponse
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
    free_tool_calculate_aspect_ratio_request = {"width":1080,"height":1350} # FreeToolCalculateAspectRatioRequest | 

    try:
        # Calculate an aspect ratio, or the missing side of an image at a given ratio
        api_response = api_instance.calculate_aspect_ratio(free_tool_calculate_aspect_ratio_request)
        print("The response of FreeToolsApi->calculate_aspect_ratio:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->calculate_aspect_ratio: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_calculate_aspect_ratio_request** | [**FreeToolCalculateAspectRatioRequest**](FreeToolCalculateAspectRatioRequest.md)|  | 

### Return type

[**FreeToolCalculateAspectRatioResponse**](FreeToolCalculateAspectRatioResponse.md)

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

# **calculate_social_roi**
> FreeToolCalculateSocialRoiResponse calculate_social_roi(free_tool_calculate_social_roi_request)

Calculate social media ROI

Calculate social media ROI. The same logic as the free web tool at https://postboost.co/tools/social-media-roi-calculator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_calculate_social_roi_request import FreeToolCalculateSocialRoiRequest
from postboost.models.free_tool_calculate_social_roi_response import FreeToolCalculateSocialRoiResponse
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
    free_tool_calculate_social_roi_request = {"revenue":5000,"costs":{"ad_spend":1000,"labor_hours":10,"hourly_rate":50}} # FreeToolCalculateSocialRoiRequest | 

    try:
        # Calculate social media ROI
        api_response = api_instance.calculate_social_roi(free_tool_calculate_social_roi_request)
        print("The response of FreeToolsApi->calculate_social_roi:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->calculate_social_roi: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_calculate_social_roi_request** | [**FreeToolCalculateSocialRoiRequest**](FreeToolCalculateSocialRoiRequest.md)|  | 

### Return type

[**FreeToolCalculateSocialRoiResponse**](FreeToolCalculateSocialRoiResponse.md)

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

# **check_link_preview**
> FreeToolCheckLinkPreviewResponse check_link_preview(free_tool_check_link_preview_request)

Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags)

Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags). The same logic as the free web tool at https://postboost.co/tools/link-preview-checker. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_check_link_preview_request import FreeToolCheckLinkPreviewRequest
from postboost.models.free_tool_check_link_preview_response import FreeToolCheckLinkPreviewResponse
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
    free_tool_check_link_preview_request = {"url":"https://example.com/features"} # FreeToolCheckLinkPreviewRequest | 

    try:
        # Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags)
        api_response = api_instance.check_link_preview(free_tool_check_link_preview_request)
        print("The response of FreeToolsApi->check_link_preview:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->check_link_preview: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_check_link_preview_request** | [**FreeToolCheckLinkPreviewRequest**](FreeToolCheckLinkPreviewRequest.md)|  | 

### Return type

[**FreeToolCheckLinkPreviewResponse**](FreeToolCheckLinkPreviewResponse.md)

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
**429** | Rate limit reached. Without a token: 30 calls per minute and 20 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute and 200 per UTC day per user. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |
**504** | The page did not load in time, or the connection failed. |  -  |

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

# **check_youtube_thumbnail**
> FreeToolCheckYoutubeThumbnailResponse check_youtube_thumbnail(free_tool_check_youtube_thumbnail_request)

Check a YouTube thumbnail's ratio, width, file size and format against YouTube's requirements

Check a YouTube thumbnail's ratio, width, file size and format against YouTube's requirements. The same logic as the free web tool at https://postboost.co/tools/youtube-thumbnail-size-checker. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_check_youtube_thumbnail_request import FreeToolCheckYoutubeThumbnailRequest
from postboost.models.free_tool_check_youtube_thumbnail_response import FreeToolCheckYoutubeThumbnailResponse
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
    free_tool_check_youtube_thumbnail_request = {"width":1280,"height":720,"file_size_bytes":921600,"format":"image/png"} # FreeToolCheckYoutubeThumbnailRequest | 

    try:
        # Check a YouTube thumbnail's ratio, width, file size and format against YouTube's requirements
        api_response = api_instance.check_youtube_thumbnail(free_tool_check_youtube_thumbnail_request)
        print("The response of FreeToolsApi->check_youtube_thumbnail:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->check_youtube_thumbnail: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_check_youtube_thumbnail_request** | [**FreeToolCheckYoutubeThumbnailRequest**](FreeToolCheckYoutubeThumbnailRequest.md)|  | 

### Return type

[**FreeToolCheckYoutubeThumbnailResponse**](FreeToolCheckYoutubeThumbnailResponse.md)

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

# **format_instagram_caption**
> FreeToolFormatInstagramCaptionResponse format_instagram_caption(free_tool_format_instagram_caption_request)

Keep blank lines in an Instagram caption with spacer lines, and count it

Keep blank lines in an Instagram caption with spacer lines, and count it. The same logic as the free web tool at https://postboost.co/tools/instagram-line-break-generator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_format_instagram_caption_request import FreeToolFormatInstagramCaptionRequest
from postboost.models.free_tool_format_instagram_caption_response import FreeToolFormatInstagramCaptionResponse
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
    free_tool_format_instagram_caption_request = {"text":"Line one\n\n\nLine two  "} # FreeToolFormatInstagramCaptionRequest | 

    try:
        # Keep blank lines in an Instagram caption with spacer lines, and count it
        api_response = api_instance.format_instagram_caption(free_tool_format_instagram_caption_request)
        print("The response of FreeToolsApi->format_instagram_caption:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->format_instagram_caption: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_format_instagram_caption_request** | [**FreeToolFormatInstagramCaptionRequest**](FreeToolFormatInstagramCaptionRequest.md)|  | 

### Return type

[**FreeToolFormatInstagramCaptionResponse**](FreeToolFormatInstagramCaptionResponse.md)

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

# **generate_hooks**
> FreeToolGenerateHooksResponse generate_hooks(free_tool_generate_hooks_request)

Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits)

Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/hook-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.free_tool_generate_hooks_request import FreeToolGenerateHooksRequest
from postboost.models.free_tool_generate_hooks_response import FreeToolGenerateHooksResponse
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
    free_tool_generate_hooks_request = {"topic":"Email newsletters for a small bakery","network":"instagram","count":2} # FreeToolGenerateHooksRequest | 

    try:
        # Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits)
        api_response = api_instance.generate_hooks(free_tool_generate_hooks_request)
        print("The response of FreeToolsApi->generate_hooks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->generate_hooks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_generate_hooks_request** | [**FreeToolGenerateHooksRequest**](FreeToolGenerateHooksRequest.md)|  | 

### Return type

[**FreeToolGenerateHooksResponse**](FreeToolGenerateHooksResponse.md)

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

# **generate_qr_code**
> FreeToolGenerateQrCodeResponse generate_qr_code(free_tool_generate_qr_code_request)

Generate a QR code (SVG) for a link or text, with optional UTM tags

Generate a QR code (SVG) for a link or text, with optional UTM tags. The same logic as the free web tool at https://postboost.co/tools/qr-code-generator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_generate_qr_code_request import FreeToolGenerateQrCodeRequest
from postboost.models.free_tool_generate_qr_code_response import FreeToolGenerateQrCodeResponse
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
    free_tool_generate_qr_code_request = {"data":"https://postboost.co","utm":{"source":"flyer"},"size":128} # FreeToolGenerateQrCodeRequest | 

    try:
        # Generate a QR code (SVG) for a link or text, with optional UTM tags
        api_response = api_instance.generate_qr_code(free_tool_generate_qr_code_request)
        print("The response of FreeToolsApi->generate_qr_code:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->generate_qr_code: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_generate_qr_code_request** | [**FreeToolGenerateQrCodeRequest**](FreeToolGenerateQrCodeRequest.md)|  | 

### Return type

[**FreeToolGenerateQrCodeResponse**](FreeToolGenerateQrCodeResponse.md)

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

# **generate_social_posts_from_blog**
> FreeToolGenerateSocialPostsFromBlogResponse generate_social_posts_from_blog(free_tool_generate_social_posts_from_blog_request)

Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits)

Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/blog-to-social-media. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). Each post spends 1 AI credit of the workspace you name (or your active workspace), so a call costs one credit per platform that comes back; results are not cached.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.free_tool_generate_social_posts_from_blog_request import FreeToolGenerateSocialPostsFromBlogRequest
from postboost.models.free_tool_generate_social_posts_from_blog_response import FreeToolGenerateSocialPostsFromBlogResponse
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
    free_tool_generate_social_posts_from_blog_request = {"url":"https://example.com/blog/utm-links","platforms":["x","linkedin"],"tone":"professional","hashtags":"few"} # FreeToolGenerateSocialPostsFromBlogRequest | 

    try:
        # Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits)
        api_response = api_instance.generate_social_posts_from_blog(free_tool_generate_social_posts_from_blog_request)
        print("The response of FreeToolsApi->generate_social_posts_from_blog:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->generate_social_posts_from_blog: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_generate_social_posts_from_blog_request** | [**FreeToolGenerateSocialPostsFromBlogRequest**](FreeToolGenerateSocialPostsFromBlogRequest.md)|  | 

### Return type

[**FreeToolGenerateSocialPostsFromBlogResponse**](FreeToolGenerateSocialPostsFromBlogResponse.md)

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

# **get_hook_templates**
> FreeToolGetHookTemplatesResponse get_hook_templates(topic=topic, category=category, network=network, search=search)

Get free hook templates for social media posts, filtered by style and network

Get free hook templates for social media posts, filtered by style and network. The same logic as the free web tool at https://postboost.co/tools/hook-generator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_get_hook_templates_response import FreeToolGetHookTemplatesResponse
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
    topic = 'topic_example' # str |  (optional)
    category = 'category_example' # str |  (optional)
    network = 'network_example' # str |  (optional)
    search = 'search_example' # str |  (optional)

    try:
        # Get free hook templates for social media posts, filtered by style and network
        api_response = api_instance.get_hook_templates(topic=topic, category=category, network=network, search=search)
        print("The response of FreeToolsApi->get_hook_templates:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->get_hook_templates: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **topic** | **str**|  | [optional] 
 **category** | **str**|  | [optional] 
 **network** | **str**|  | [optional] 
 **search** | **str**|  | [optional] 

### Return type

[**FreeToolGetHookTemplatesResponse**](FreeToolGetHookTemplatesResponse.md)

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

# **get_video_specs**
> FreeToolGetVideoSpecsResponse get_video_specs(network=network)

Get social media video ratios, resolutions, lengths and file size limits per network, with sources

Get social media video ratios, resolutions, lengths and file size limits per network, with sources. The same logic as the free web tool at https://postboost.co/tools/social-media-video-specs. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_get_video_specs_response import FreeToolGetVideoSpecsResponse
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
        # Get social media video ratios, resolutions, lengths and file size limits per network, with sources
        api_response = api_instance.get_video_specs(network=network)
        print("The response of FreeToolsApi->get_video_specs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->get_video_specs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **network** | **str**|  | [optional] 

### Return type

[**FreeToolGetVideoSpecsResponse**](FreeToolGetVideoSpecsResponse.md)

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

# **plan_content_calendar**
> FreeToolPlanContentCalendarResponse plan_content_calendar(free_tool_plan_content_calendar_request)

Plan a social media content calendar and get it as CSV and ICS

Plan a social media content calendar and get it as CSV and ICS. The same logic as the free web tool at https://postboost.co/tools/social-media-content-calendar-generator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_plan_content_calendar_request import FreeToolPlanContentCalendarRequest
from postboost.models.free_tool_plan_content_calendar_response import FreeToolPlanContentCalendarResponse
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
    free_tool_plan_content_calendar_request = {"start_date":"2026-11-02","weeks":1,"posts_per_week":{"instagram":3,"linkedin":2},"times":{"linkedin":"08:30"},"pillars":["Tips","Product"]} # FreeToolPlanContentCalendarRequest | 

    try:
        # Plan a social media content calendar and get it as CSV and ICS
        api_response = api_instance.plan_content_calendar(free_tool_plan_content_calendar_request)
        print("The response of FreeToolsApi->plan_content_calendar:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->plan_content_calendar: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_plan_content_calendar_request** | [**FreeToolPlanContentCalendarRequest**](FreeToolPlanContentCalendarRequest.md)|  | 

### Return type

[**FreeToolPlanContentCalendarResponse**](FreeToolPlanContentCalendarResponse.md)

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

# **preview_post**
> FreeToolPreviewPostResponse preview_post(free_tool_preview_post_request)

Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook

Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook. The same logic as the free web tool at https://postboost.co/tools/social-media-post-preview. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_preview_post_request import FreeToolPreviewPostRequest
from postboost.models.free_tool_preview_post_response import FreeToolPreviewPostResponse
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
    free_tool_preview_post_request = {"text":"New feature: schedule a month of posts in one sitting."} # FreeToolPreviewPostRequest | 

    try:
        # Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook
        api_response = api_instance.preview_post(free_tool_preview_post_request)
        print("The response of FreeToolsApi->preview_post:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->preview_post: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_preview_post_request** | [**FreeToolPreviewPostRequest**](FreeToolPreviewPostRequest.md)|  | 

### Return type

[**FreeToolPreviewPostResponse**](FreeToolPreviewPostResponse.md)

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


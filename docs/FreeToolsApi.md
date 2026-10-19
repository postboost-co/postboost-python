# postboost.FreeToolsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**build_hashtag_groups**](FreeToolsApi.md#build_hashtag_groups) | **POST** /tools/hashtag-group-builder | Clean, dedupe and split hashtags into groups that fit a network&#39;s hashtag cap
[**build_utm_url**](FreeToolsApi.md#build_utm_url) | **POST** /tools/utm-builder | Build a UTM-tagged campaign URL
[**calculate_aspect_ratio**](FreeToolsApi.md#calculate_aspect_ratio) | **POST** /tools/aspect-ratio-calculator | Calculate an aspect ratio, or the missing side of an image at a given ratio
[**calculate_carousel_slices**](FreeToolsApi.md#calculate_carousel_slices) | **POST** /tools/instagram-carousel-splitter | Split a wide image into seamless Instagram carousel slides
[**calculate_crop**](FreeToolsApi.md#calculate_crop) | **POST** /tools/social-media-image-sizes/crop | Calculate the crop box that fits an image to a social media size
[**calculate_engagement_rate**](FreeToolsApi.md#calculate_engagement_rate) | **POST** /tools/engagement-rate-calculator | Calculate an engagement rate
[**calculate_influencer_rate**](FreeToolsApi.md#calculate_influencer_rate) | **POST** /tools/influencer-rate-calculator | Estimate an influencer&#39;s rate for one sponsored deliverable
[**calculate_smm_pricing**](FreeToolsApi.md#calculate_smm_pricing) | **POST** /tools/social-media-manager-pricing-calculator | Estimate social media manager pricing
[**calculate_social_roi**](FreeToolsApi.md#calculate_social_roi) | **POST** /tools/social-media-roi-calculator | Calculate social media ROI
[**calculate_x_api_cost**](FreeToolsApi.md#calculate_x_api_cost) | **POST** /tools/x-api-cost-calculator | Calculate the monthly X API cost
[**check_link_preview**](FreeToolsApi.md#check_link_preview) | **POST** /tools/link-preview-checker | Check how a link previews on X, LinkedIn, Facebook and chat apps (Open Graph and Twitter card tags)
[**check_post**](FreeToolsApi.md#check_post) | **POST** /tools/social-media-post-checker | Check a post against each network&#39;s publishing rules
[**check_readability**](FreeToolsApi.md#check_readability) | **POST** /tools/post-readability-checker | Check the readability of a post: Flesch scores, long sentences and passive hints
[**check_youtube_thumbnail**](FreeToolsApi.md#check_youtube_thumbnail) | **POST** /tools/youtube-thumbnail-size-checker | Check a YouTube thumbnail&#39;s ratio, width, file size and format against YouTube&#39;s requirements
[**clean_text**](FreeToolsApi.md#clean_text) | **POST** /tools/ai-text-cleaner | Clean AI-written text: dashes, quotes, invisible characters, markdown
[**count_characters**](FreeToolsApi.md#count_characters) | **POST** /tools/social-media-character-counter | Count characters as each network counts them
[**find_automation_recipes**](FreeToolsApi.md#find_automation_recipes) | **GET** /tools/social-media-automation-recipes | Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API
[**format_instagram_caption**](FreeToolsApi.md#format_instagram_caption) | **POST** /tools/instagram-line-break-generator | Keep blank lines in an Instagram caption with spacer lines, and count it
[**format_linked_in_post**](FreeToolsApi.md#format_linked_in_post) | **POST** /tools/linkedin-post-formatter | Format a LinkedIn post with bold, italic and lists
[**generate_alt_text**](FreeToolsApi.md#generate_alt_text) | **POST** /tools/alt-text-generator | Write alt text for an image with AI (needs a token, spends AI credits)
[**generate_bio**](FreeToolsApi.md#generate_bio) | **POST** /tools/instagram-bio-generator | Write five profile bios with AI (needs a token, spends AI credits)
[**generate_caption**](FreeToolsApi.md#generate_caption) | **POST** /tools/instagram-caption-generator | Write three post captions for a topic with AI (needs a token, spends AI credits)
[**generate_fancy_text**](FreeToolsApi.md#generate_fancy_text) | **POST** /tools/fancy-text-generator | Convert text to fancy Unicode styles
[**generate_hashtags**](FreeToolsApi.md#generate_hashtags) | **POST** /tools/instagram-hashtag-generator | Generate hashtags for a post topic with AI (needs a token, spends AI credits)
[**generate_hooks**](FreeToolsApi.md#generate_hooks) | **POST** /tools/hook-generator | Generate hooks (opening lines) for a social media post with AI (needs a token, spends AI credits)
[**generate_linked_in_headline**](FreeToolsApi.md#generate_linked_in_headline) | **POST** /tools/linkedin-headline-generator | Write five LinkedIn profile headlines with AI (needs a token, spends AI credits)
[**generate_qr_code**](FreeToolsApi.md#generate_qr_code) | **POST** /tools/qr-code-generator | Generate a QR code (SVG) for a link or text, with optional UTM tags
[**generate_social_posts_from_blog**](FreeToolsApi.md#generate_social_posts_from_blog) | **POST** /tools/blog-to-social-media | Turn a blog post (URL or text) into one social post per network with AI (needs a token, spends AI credits)
[**generate_usernames**](FreeToolsApi.md#generate_usernames) | **POST** /tools/social-media-username-generator | Generate social media usernames
[**generate_youtube_description**](FreeToolsApi.md#generate_youtube_description) | **POST** /tools/youtube-description-generator | Write three YouTube video descriptions with AI (needs a token, spends AI credits)
[**generate_youtube_titles**](FreeToolsApi.md#generate_youtube_titles) | **POST** /tools/youtube-title-generator | Write five YouTube video titles with AI (needs a token, spends AI credits)
[**get_best_times_to_post**](FreeToolsApi.md#get_best_times_to_post) | **GET** /tools/best-time-to-post | Get the best times to post per network from published studies, with sources
[**get_glossary**](FreeToolsApi.md#get_glossary) | **GET** /tools/social-media-glossary | Look up social media terms: plain-language definitions by category, with sources and related terms
[**get_hook_templates**](FreeToolsApi.md#get_hook_templates) | **GET** /tools/hook-generator/library | Get free hook templates for social media posts, filtered by style and network
[**get_image_sizes**](FreeToolsApi.md#get_image_sizes) | **GET** /tools/social-media-image-sizes | Get social media image sizes per network, each with its source
[**get_safe_zones**](FreeToolsApi.md#get_safe_zones) | **POST** /tools/safe-zone-checker | Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame
[**get_video_specs**](FreeToolsApi.md#get_video_specs) | **GET** /tools/social-media-video-specs | Get social media video ratios, resolutions, lengths and file size limits per network, with sources
[**list_awareness_days**](FreeToolsApi.md#list_awareness_days) | **GET** /tools/social-media-holiday-calendar | List public holidays, awareness days and social media days by date, country, type and topic, with sources
[**list_free_tools**](FreeToolsApi.md#list_free_tools) | **GET** /tools | List the free tools
[**pick_social_media_tool**](FreeToolsApi.md#pick_social_media_tool) | **POST** /tools/social-media-tool-picker | Match your needs against social media management tools and see what each one misses
[**plan_content_calendar**](FreeToolsApi.md#plan_content_calendar) | **POST** /tools/social-media-content-calendar-generator | Plan a social media content calendar and get it as CSV and ICS
[**plan_posting_frequency**](FreeToolsApi.md#plan_posting_frequency) | **POST** /tools/posting-frequency-planner | Plan how often to post on each network
[**preview_post**](FreeToolsApi.md#preview_post) | **POST** /tools/social-media-post-preview | Preview where a post folds and when its image is cropped on Instagram, X, LinkedIn and Facebook
[**score_social_audit**](FreeToolsApi.md#score_social_audit) | **POST** /tools/social-media-audit-template | Score a social media audit checklist and get the top fixes
[**search_emoji**](FreeToolsApi.md#search_emoji) | **POST** /tools/social-media-emoji-picker | Search emoji by name or keyword, to copy and paste into a post
[**split_thread**](FreeToolsApi.md#split_thread) | **POST** /tools/x-thread-maker | Split long text into a thread
[**summarize_report**](FreeToolsApi.md#summarize_report) | **POST** /tools/social-media-report-generator | Summarize social media post metrics into a report
[**verify_webhook_signature**](FreeToolsApi.md#verify_webhook_signature) | **POST** /tools/webhook-signature-verifier | Verify an HMAC webhook signature


# **build_hashtag_groups**
> FreeToolBuildHashtagGroupsResponse build_hashtag_groups(free_tool_build_hashtag_groups_request)

Clean, dedupe and split hashtags into groups that fit a network's hashtag cap

Clean, dedupe and split hashtags into groups that fit a network's hashtag cap. The same logic as the free web tool at https://postboost.co/tools/hashtag-group-builder. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_build_hashtag_groups_request import FreeToolBuildHashtagGroupsRequest
from postboost.models.free_tool_build_hashtag_groups_response import FreeToolBuildHashtagGroupsResponse
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
    free_tool_build_hashtag_groups_request = {"text":"travel, #Travel  #travel_tips 2026 #photo!graphy"} # FreeToolBuildHashtagGroupsRequest | 

    try:
        # Clean, dedupe and split hashtags into groups that fit a network's hashtag cap
        api_response = api_instance.build_hashtag_groups(free_tool_build_hashtag_groups_request)
        print("The response of FreeToolsApi->build_hashtag_groups:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->build_hashtag_groups: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_build_hashtag_groups_request** | [**FreeToolBuildHashtagGroupsRequest**](FreeToolBuildHashtagGroupsRequest.md)|  | 

### Return type

[**FreeToolBuildHashtagGroupsResponse**](FreeToolBuildHashtagGroupsResponse.md)

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

# **calculate_carousel_slices**
> FreeToolCalculateCarouselSlicesResponse calculate_carousel_slices(free_tool_calculate_carousel_slices_request)

Split a wide image into seamless Instagram carousel slides

Split a wide image into seamless Instagram carousel slides. The same logic as the free web tool at https://postboost.co/tools/instagram-carousel-splitter. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_calculate_carousel_slices_request import FreeToolCalculateCarouselSlicesRequest
from postboost.models.free_tool_calculate_carousel_slices_response import FreeToolCalculateCarouselSlicesResponse
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
    free_tool_calculate_carousel_slices_request = {"width":3240,"height":1350,"slides":3,"ratio":"4:5"} # FreeToolCalculateCarouselSlicesRequest | 

    try:
        # Split a wide image into seamless Instagram carousel slides
        api_response = api_instance.calculate_carousel_slices(free_tool_calculate_carousel_slices_request)
        print("The response of FreeToolsApi->calculate_carousel_slices:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->calculate_carousel_slices: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_calculate_carousel_slices_request** | [**FreeToolCalculateCarouselSlicesRequest**](FreeToolCalculateCarouselSlicesRequest.md)|  | 

### Return type

[**FreeToolCalculateCarouselSlicesResponse**](FreeToolCalculateCarouselSlicesResponse.md)

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

# **calculate_influencer_rate**
> FreeToolCalculateInfluencerRateResponse calculate_influencer_rate(free_tool_calculate_influencer_rate_request)

Estimate an influencer's rate for one sponsored deliverable

Estimate an influencer's rate for one sponsored deliverable. The same logic as the free web tool at https://postboost.co/tools/influencer-rate-calculator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_calculate_influencer_rate_request import FreeToolCalculateInfluencerRateRequest
from postboost.models.free_tool_calculate_influencer_rate_response import FreeToolCalculateInfluencerRateResponse
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
    free_tool_calculate_influencer_rate_request = {"network":"instagram","followers":25000,"deliverable":"reel","usage_rights_months":3} # FreeToolCalculateInfluencerRateRequest | 

    try:
        # Estimate an influencer's rate for one sponsored deliverable
        api_response = api_instance.calculate_influencer_rate(free_tool_calculate_influencer_rate_request)
        print("The response of FreeToolsApi->calculate_influencer_rate:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->calculate_influencer_rate: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_calculate_influencer_rate_request** | [**FreeToolCalculateInfluencerRateRequest**](FreeToolCalculateInfluencerRateRequest.md)|  | 

### Return type

[**FreeToolCalculateInfluencerRateResponse**](FreeToolCalculateInfluencerRateResponse.md)

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

# **calculate_smm_pricing**
> FreeToolCalculateSmmPricingResponse calculate_smm_pricing(free_tool_calculate_smm_pricing_request)

Estimate social media manager pricing

Estimate social media manager pricing. The same logic as the free web tool at https://postboost.co/tools/social-media-manager-pricing-calculator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_calculate_smm_pricing_request import FreeToolCalculateSmmPricingRequest
from postboost.models.free_tool_calculate_smm_pricing_response import FreeToolCalculateSmmPricingResponse
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
    free_tool_calculate_smm_pricing_request = {"networks":3,"posts_per_week":5,"content_type":"copy_design","community_hours_per_week":4,"hourly_rate":50} # FreeToolCalculateSmmPricingRequest | 

    try:
        # Estimate social media manager pricing
        api_response = api_instance.calculate_smm_pricing(free_tool_calculate_smm_pricing_request)
        print("The response of FreeToolsApi->calculate_smm_pricing:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->calculate_smm_pricing: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_calculate_smm_pricing_request** | [**FreeToolCalculateSmmPricingRequest**](FreeToolCalculateSmmPricingRequest.md)|  | 

### Return type

[**FreeToolCalculateSmmPricingResponse**](FreeToolCalculateSmmPricingResponse.md)

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

# **calculate_x_api_cost**
> FreeToolCalculateXApiCostResponse calculate_x_api_cost(free_tool_calculate_x_api_cost_request)

Calculate the monthly X API cost

Calculate the monthly X API cost. The same logic as the free web tool at https://postboost.co/tools/x-api-cost-calculator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_calculate_x_api_cost_request import FreeToolCalculateXApiCostRequest
from postboost.models.free_tool_calculate_x_api_cost_response import FreeToolCalculateXApiCostResponse
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
    free_tool_calculate_x_api_cost_request = {"posts":1000,"link_share":20} # FreeToolCalculateXApiCostRequest | 

    try:
        # Calculate the monthly X API cost
        api_response = api_instance.calculate_x_api_cost(free_tool_calculate_x_api_cost_request)
        print("The response of FreeToolsApi->calculate_x_api_cost:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->calculate_x_api_cost: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_calculate_x_api_cost_request** | [**FreeToolCalculateXApiCostRequest**](FreeToolCalculateXApiCostRequest.md)|  | 

### Return type

[**FreeToolCalculateXApiCostResponse**](FreeToolCalculateXApiCostResponse.md)

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

# **check_readability**
> FreeToolCheckReadabilityResponse check_readability(free_tool_check_readability_request)

Check the readability of a post: Flesch scores, long sentences and passive hints

Check the readability of a post: Flesch scores, long sentences and passive hints. The same logic as the free web tool at https://postboost.co/tools/post-readability-checker. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_check_readability_request import FreeToolCheckReadabilityRequest
from postboost.models.free_tool_check_readability_response import FreeToolCheckReadabilityResponse
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
    free_tool_check_readability_request = {"text":"The cat sat on the mat. 🐱 #cats"} # FreeToolCheckReadabilityRequest | 

    try:
        # Check the readability of a post: Flesch scores, long sentences and passive hints
        api_response = api_instance.check_readability(free_tool_check_readability_request)
        print("The response of FreeToolsApi->check_readability:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->check_readability: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_check_readability_request** | [**FreeToolCheckReadabilityRequest**](FreeToolCheckReadabilityRequest.md)|  | 

### Return type

[**FreeToolCheckReadabilityResponse**](FreeToolCheckReadabilityResponse.md)

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

# **find_automation_recipes**
> FreeToolFindAutomationRecipesResponse find_automation_recipes(platform=platform, trigger=trigger, q=q)

Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API

Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API. The same logic as the free web tool at https://postboost.co/tools/social-media-automation-recipes. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_find_automation_recipes_response import FreeToolFindAutomationRecipesResponse
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
    platform = 'platform_example' # str |  (optional)
    trigger = 'trigger_example' # str |  (optional)
    q = 'q_example' # str |  (optional)

    try:
        # Find n8n, Zapier and Make recipes that automate social media posting through the PostBoost API
        api_response = api_instance.find_automation_recipes(platform=platform, trigger=trigger, q=q)
        print("The response of FreeToolsApi->find_automation_recipes:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->find_automation_recipes: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platform** | **str**|  | [optional] 
 **trigger** | **str**|  | [optional] 
 **q** | **str**|  | [optional] 

### Return type

[**FreeToolFindAutomationRecipesResponse**](FreeToolFindAutomationRecipesResponse.md)

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

# **generate_alt_text**
> FreeToolGenerateAltTextResponse generate_alt_text(free_tool_generate_alt_text_request)

Write alt text for an image with AI (needs a token, spends AI credits)

Write alt text for an image with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/alt-text-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.free_tool_generate_alt_text_request import FreeToolGenerateAltTextRequest
from postboost.models.free_tool_generate_alt_text_response import FreeToolGenerateAltTextResponse
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
    free_tool_generate_alt_text_request = {"image_url":"https://example.com/images/sourdough.jpg","context":"our bakery opens on Saturday","length":"short"} # FreeToolGenerateAltTextRequest | 

    try:
        # Write alt text for an image with AI (needs a token, spends AI credits)
        api_response = api_instance.generate_alt_text(free_tool_generate_alt_text_request)
        print("The response of FreeToolsApi->generate_alt_text:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->generate_alt_text: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_generate_alt_text_request** | [**FreeToolGenerateAltTextRequest**](FreeToolGenerateAltTextRequest.md)|  | 

### Return type

[**FreeToolGenerateAltTextResponse**](FreeToolGenerateAltTextResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json, multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The tool output. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  |
**401** | No API token, or an invalid one. The body has &#x60;register_url&#x60; to create a free account. |  -  |
**403** | &#x60;workspace&#x60; is not a workspace you belong to, or your account has no workspace, or a scoped API key lacks the &#x60;ai&#x60; ability or is bound to another workspace (&#x60;code: insufficient_scope&#x60;). |  -  |
**413** | The request body is larger than 7 MB. |  -  |
**422** |  |  -  |
**429** | The workspace has no AI credits left this billing cycle (&#x60;code: ai_credits_exhausted&#x60;, &#x60;upgrade_url&#x60;), or the per-minute limit was reached. Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |
**502** | The AI provider failed or timed out. No credit was spent. |  -  |
**503** | AI tools are switched off right now. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_bio**
> FreeToolGenerateBioResponse generate_bio(free_tool_generate_bio_request)

Write five profile bios with AI (needs a token, spends AI credits)

Write five profile bios with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/instagram-bio-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.free_tool_generate_bio_request import FreeToolGenerateBioRequest
from postboost.models.free_tool_generate_bio_response import FreeToolGenerateBioResponse
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
    free_tool_generate_bio_request = {"text":"Wedding photographer for small weddings in Lisbon","tone":"friendly"} # FreeToolGenerateBioRequest | 

    try:
        # Write five profile bios with AI (needs a token, spends AI credits)
        api_response = api_instance.generate_bio(free_tool_generate_bio_request)
        print("The response of FreeToolsApi->generate_bio:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->generate_bio: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_generate_bio_request** | [**FreeToolGenerateBioRequest**](FreeToolGenerateBioRequest.md)|  | 

### Return type

[**FreeToolGenerateBioResponse**](FreeToolGenerateBioResponse.md)

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

# **generate_linked_in_headline**
> FreeToolGenerateLinkedInHeadlineResponse generate_linked_in_headline(free_tool_generate_linked_in_headline_request)

Write five LinkedIn profile headlines with AI (needs a token, spends AI credits)

Write five LinkedIn profile headlines with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/linkedin-headline-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.free_tool_generate_linked_in_headline_request import FreeToolGenerateLinkedInHeadlineRequest
from postboost.models.free_tool_generate_linked_in_headline_response import FreeToolGenerateLinkedInHeadlineResponse
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
    free_tool_generate_linked_in_headline_request = {"role":"Customer success lead","skills":"B2B SaaS onboarding, churn analysis, customer training","audience":"SaaS founders"} # FreeToolGenerateLinkedInHeadlineRequest | 

    try:
        # Write five LinkedIn profile headlines with AI (needs a token, spends AI credits)
        api_response = api_instance.generate_linked_in_headline(free_tool_generate_linked_in_headline_request)
        print("The response of FreeToolsApi->generate_linked_in_headline:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->generate_linked_in_headline: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_generate_linked_in_headline_request** | [**FreeToolGenerateLinkedInHeadlineRequest**](FreeToolGenerateLinkedInHeadlineRequest.md)|  | 

### Return type

[**FreeToolGenerateLinkedInHeadlineResponse**](FreeToolGenerateLinkedInHeadlineResponse.md)

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

# **generate_usernames**
> FreeToolGenerateUsernamesResponse generate_usernames(free_tool_generate_usernames_request)

Generate social media usernames

Generate social media usernames. The same logic as the free web tool at https://postboost.co/tools/social-media-username-generator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_generate_usernames_request import FreeToolGenerateUsernamesRequest
from postboost.models.free_tool_generate_usernames_response import FreeToolGenerateUsernamesResponse
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
    free_tool_generate_usernames_request = {"name":"Maya Green"} # FreeToolGenerateUsernamesRequest | 

    try:
        # Generate social media usernames
        api_response = api_instance.generate_usernames(free_tool_generate_usernames_request)
        print("The response of FreeToolsApi->generate_usernames:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->generate_usernames: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_generate_usernames_request** | [**FreeToolGenerateUsernamesRequest**](FreeToolGenerateUsernamesRequest.md)|  | 

### Return type

[**FreeToolGenerateUsernamesResponse**](FreeToolGenerateUsernamesResponse.md)

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

# **generate_youtube_description**
> FreeToolGenerateYoutubeDescriptionResponse generate_youtube_description(free_tool_generate_youtube_description_request)

Write three YouTube video descriptions with AI (needs a token, spends AI credits)

Write three YouTube video descriptions with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/youtube-description-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.free_tool_generate_youtube_description_request import FreeToolGenerateYoutubeDescriptionRequest
from postboost.models.free_tool_generate_youtube_description_response import FreeToolGenerateYoutubeDescriptionResponse
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
    free_tool_generate_youtube_description_request = {"text":"A beginner sourdough bread recipe: feeding the starter, mixing, shaping and baking in a Dutch oven.","keywords":"sourdough bread, beginner","chapters":true,"chapter_lines":["0:00 Intro","1:30 Feeding the starter","4:10 Shaping","9:45 Baking"],"cta":"subscribe"} # FreeToolGenerateYoutubeDescriptionRequest | 

    try:
        # Write three YouTube video descriptions with AI (needs a token, spends AI credits)
        api_response = api_instance.generate_youtube_description(free_tool_generate_youtube_description_request)
        print("The response of FreeToolsApi->generate_youtube_description:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->generate_youtube_description: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_generate_youtube_description_request** | [**FreeToolGenerateYoutubeDescriptionRequest**](FreeToolGenerateYoutubeDescriptionRequest.md)|  | 

### Return type

[**FreeToolGenerateYoutubeDescriptionResponse**](FreeToolGenerateYoutubeDescriptionResponse.md)

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

# **generate_youtube_titles**
> FreeToolGenerateYoutubeTitlesResponse generate_youtube_titles(free_tool_generate_youtube_titles_request)

Write five YouTube video titles with AI (needs a token, spends AI credits)

Write five YouTube video titles with AI (needs a token, spends AI credits). The same logic as the free web tool at https://postboost.co/tools/youtube-title-generator. Needs an API token (a scoped key needs the `ai` ability and pays with its own workspace). A new generation spends 1 AI credit of the workspace you name (or your active workspace); a repeated identical request is answered from the cache for free.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.free_tool_generate_youtube_titles_request import FreeToolGenerateYoutubeTitlesRequest
from postboost.models.free_tool_generate_youtube_titles_response import FreeToolGenerateYoutubeTitlesResponse
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
    free_tool_generate_youtube_titles_request = {"text":"Baking sourdough bread at home for beginners","style":"how-to"} # FreeToolGenerateYoutubeTitlesRequest | 

    try:
        # Write five YouTube video titles with AI (needs a token, spends AI credits)
        api_response = api_instance.generate_youtube_titles(free_tool_generate_youtube_titles_request)
        print("The response of FreeToolsApi->generate_youtube_titles:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->generate_youtube_titles: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_generate_youtube_titles_request** | [**FreeToolGenerateYoutubeTitlesRequest**](FreeToolGenerateYoutubeTitlesRequest.md)|  | 

### Return type

[**FreeToolGenerateYoutubeTitlesResponse**](FreeToolGenerateYoutubeTitlesResponse.md)

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

# **get_glossary**
> FreeToolGetGlossaryResponse get_glossary(q=q, category=category)

Look up social media terms: plain-language definitions by category, with sources and related terms

Look up social media terms: plain-language definitions by category, with sources and related terms. The same logic as the free web tool at https://postboost.co/tools/social-media-glossary. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_get_glossary_response import FreeToolGetGlossaryResponse
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
    q = 'q_example' # str |  (optional)
    category = 'category_example' # str |  (optional)

    try:
        # Look up social media terms: plain-language definitions by category, with sources and related terms
        api_response = api_instance.get_glossary(q=q, category=category)
        print("The response of FreeToolsApi->get_glossary:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->get_glossary: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **q** | **str**|  | [optional] 
 **category** | **str**|  | [optional] 

### Return type

[**FreeToolGetGlossaryResponse**](FreeToolGetGlossaryResponse.md)

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

# **get_safe_zones**
> FreeToolGetSafeZonesResponse get_safe_zones(free_tool_get_safe_zones_request)

Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame

Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame. The same logic as the free web tool at https://postboost.co/tools/safe-zone-checker. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_get_safe_zones_request import FreeToolGetSafeZonesRequest
from postboost.models.free_tool_get_safe_zones_response import FreeToolGetSafeZonesResponse
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
    free_tool_get_safe_zones_request = {"platform":"tiktok"} # FreeToolGetSafeZonesRequest | 

    try:
        # Get the TikTok, Instagram Reels or YouTube Shorts safe zones for a vertical frame
        api_response = api_instance.get_safe_zones(free_tool_get_safe_zones_request)
        print("The response of FreeToolsApi->get_safe_zones:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->get_safe_zones: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_get_safe_zones_request** | [**FreeToolGetSafeZonesRequest**](FreeToolGetSafeZonesRequest.md)|  | 

### Return type

[**FreeToolGetSafeZonesResponse**](FreeToolGetSafeZonesResponse.md)

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

# **list_awareness_days**
> FreeToolListAwarenessDaysResponse list_awareness_days(var_from=var_from, to=to, country=country, type=type, topic=topic)

List public holidays, awareness days and social media days by date, country, type and topic, with sources

List public holidays, awareness days and social media days by date, country, type and topic, with sources. The same logic as the free web tool at https://postboost.co/tools/social-media-holiday-calendar. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_list_awareness_days_response import FreeToolListAwarenessDaysResponse
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
    var_from = 'var_from_example' # str |  (optional)
    to = 'to_example' # str |  (optional)
    country = 'country_example' # str |  (optional)
    type = 'type_example' # str |  (optional)
    topic = 'topic_example' # str |  (optional)

    try:
        # List public holidays, awareness days and social media days by date, country, type and topic, with sources
        api_response = api_instance.list_awareness_days(var_from=var_from, to=to, country=country, type=type, topic=topic)
        print("The response of FreeToolsApi->list_awareness_days:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->list_awareness_days: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **var_from** | **str**|  | [optional] 
 **to** | **str**|  | [optional] 
 **country** | **str**|  | [optional] 
 **type** | **str**|  | [optional] 
 **topic** | **str**|  | [optional] 

### Return type

[**FreeToolListAwarenessDaysResponse**](FreeToolListAwarenessDaysResponse.md)

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

# **pick_social_media_tool**
> FreeToolPickSocialMediaToolResponse pick_social_media_tool(free_tool_pick_social_media_tool_request)

Match your needs against social media management tools and see what each one misses

Match your needs against social media management tools and see what each one misses. The same logic as the free web tool at https://postboost.co/tools/social-media-tool-picker. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_pick_social_media_tool_request import FreeToolPickSocialMediaToolRequest
from postboost.models.free_tool_pick_social_media_tool_response import FreeToolPickSocialMediaToolResponse
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
    free_tool_pick_social_media_tool_request = {"needs":["rest_openapi","mcp","webhooks","free_tier"]} # FreeToolPickSocialMediaToolRequest | 

    try:
        # Match your needs against social media management tools and see what each one misses
        api_response = api_instance.pick_social_media_tool(free_tool_pick_social_media_tool_request)
        print("The response of FreeToolsApi->pick_social_media_tool:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->pick_social_media_tool: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_pick_social_media_tool_request** | [**FreeToolPickSocialMediaToolRequest**](FreeToolPickSocialMediaToolRequest.md)|  | 

### Return type

[**FreeToolPickSocialMediaToolResponse**](FreeToolPickSocialMediaToolResponse.md)

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

# **plan_posting_frequency**
> FreeToolPlanPostingFrequencyResponse plan_posting_frequency(free_tool_plan_posting_frequency_request)

Plan how often to post on each network

Plan how often to post on each network. The same logic as the free web tool at https://postboost.co/tools/posting-frequency-planner. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_plan_posting_frequency_request import FreeToolPlanPostingFrequencyRequest
from postboost.models.free_tool_plan_posting_frequency_response import FreeToolPlanPostingFrequencyResponse
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
    free_tool_plan_posting_frequency_request = {"networks":["instagram","linkedin","tiktok"],"posts_per_week_capacity":12} # FreeToolPlanPostingFrequencyRequest | 

    try:
        # Plan how often to post on each network
        api_response = api_instance.plan_posting_frequency(free_tool_plan_posting_frequency_request)
        print("The response of FreeToolsApi->plan_posting_frequency:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->plan_posting_frequency: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_plan_posting_frequency_request** | [**FreeToolPlanPostingFrequencyRequest**](FreeToolPlanPostingFrequencyRequest.md)|  | 

### Return type

[**FreeToolPlanPostingFrequencyResponse**](FreeToolPlanPostingFrequencyResponse.md)

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

# **score_social_audit**
> FreeToolScoreSocialAuditResponse score_social_audit(free_tool_score_social_audit_request)

Score a social media audit checklist and get the top fixes

Score a social media audit checklist and get the top fixes. The same logic as the free web tool at https://postboost.co/tools/social-media-audit-template. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_score_social_audit_request import FreeToolScoreSocialAuditRequest
from postboost.models.free_tool_score_social_audit_response import FreeToolScoreSocialAuditResponse
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
    free_tool_score_social_audit_request = {"target_posts_per_week":4,"instagram":{"profile":"yes","bio":"yes","link_tracking":"no","frequency":"partly","replies":"yes","native_formats":"yes","pinned":"no","engagement_rate":"partly"},"linkedin":{"profile":"yes","bio":"partly","link_tracking":"no","frequency":"yes","replies":"partly","native_formats":"no","pinned":"yes","engagement_rate":"no"}} # FreeToolScoreSocialAuditRequest | 

    try:
        # Score a social media audit checklist and get the top fixes
        api_response = api_instance.score_social_audit(free_tool_score_social_audit_request)
        print("The response of FreeToolsApi->score_social_audit:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->score_social_audit: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_score_social_audit_request** | [**FreeToolScoreSocialAuditRequest**](FreeToolScoreSocialAuditRequest.md)|  | 

### Return type

[**FreeToolScoreSocialAuditResponse**](FreeToolScoreSocialAuditResponse.md)

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

# **search_emoji**
> FreeToolSearchEmojiResponse search_emoji(free_tool_search_emoji_request)

Search emoji by name or keyword, to copy and paste into a post

Search emoji by name or keyword, to copy and paste into a post. The same logic as the free web tool at https://postboost.co/tools/social-media-emoji-picker. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_search_emoji_request import FreeToolSearchEmojiRequest
from postboost.models.free_tool_search_emoji_response import FreeToolSearchEmojiResponse
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
    free_tool_search_emoji_request = {"query":"fire","limit":2} # FreeToolSearchEmojiRequest | 

    try:
        # Search emoji by name or keyword, to copy and paste into a post
        api_response = api_instance.search_emoji(free_tool_search_emoji_request)
        print("The response of FreeToolsApi->search_emoji:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->search_emoji: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_search_emoji_request** | [**FreeToolSearchEmojiRequest**](FreeToolSearchEmojiRequest.md)|  | 

### Return type

[**FreeToolSearchEmojiResponse**](FreeToolSearchEmojiResponse.md)

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

# **summarize_report**
> FreeToolSummarizeReportResponse summarize_report(free_tool_summarize_report_request)

Summarize social media post metrics into a report

Summarize social media post metrics into a report. The same logic as the free web tool at https://postboost.co/tools/social-media-report-generator. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_summarize_report_request import FreeToolSummarizeReportRequest
from postboost.models.free_tool_summarize_report_response import FreeToolSummarizeReportResponse
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
    free_tool_summarize_report_request = {"rows":[{"date":"2026-09-01","network":"linkedin","text":"Launch post: our new planning board","views":2400,"likes":96,"comments":12,"shares":8},{"date":"2026-09-02","network":"instagram","text":"Behind the scenes of the shoot","views":1800,"likes":120,"comments":9,"shares":3},{"date":"2026-09-08","network":"linkedin","text":"Customer story: a bakery's bookings","views":1500,"likes":40,"comments":4,"shares":6}]} # FreeToolSummarizeReportRequest | 

    try:
        # Summarize social media post metrics into a report
        api_response = api_instance.summarize_report(free_tool_summarize_report_request)
        print("The response of FreeToolsApi->summarize_report:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->summarize_report: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_summarize_report_request** | [**FreeToolSummarizeReportRequest**](FreeToolSummarizeReportRequest.md)|  | 

### Return type

[**FreeToolSummarizeReportResponse**](FreeToolSummarizeReportResponse.md)

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
**413** | The request body is larger than 2 MB. |  -  |
**422** |  |  -  |
**429** | Rate limit reached. Without a token: 30 calls per minute and 500 per UTC day per IP address (IPv6 per /64). With a token: 300 per minute per user; the Free plan also has 1,000 calls per UTC day, paid plans have no daily cap. |  * X-RateLimit-Limit - Calls allowed in the limit window closest to running out. <br>  * X-RateLimit-Remaining - Calls left in that window. <br>  * Retry-After - Seconds until the limit resets. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_webhook_signature**
> FreeToolVerifyWebhookSignatureResponse verify_webhook_signature(free_tool_verify_webhook_signature_request)

Verify an HMAC webhook signature

Verify an HMAC webhook signature. The same logic as the free web tool at https://postboost.co/tools/webhook-signature-verifier. No account needed: call it without a token, or with any API token.

### Example


```python
import postboost
from postboost.models.free_tool_verify_webhook_signature_request import FreeToolVerifyWebhookSignatureRequest
from postboost.models.free_tool_verify_webhook_signature_response import FreeToolVerifyWebhookSignatureResponse
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
    free_tool_verify_webhook_signature_request = {"body":"{\"event\":\"post.published\",\"data\":{\"uuid\":\"0b8f1c2e-6c1d-4f7a-9a51-3d1e2f4a5b6c\"}}","secret":"whsec_test","signature":"a27f6d074108ea6b5df903d3ad4520113a47aa3710cb26c24fab7e36457d915a"} # FreeToolVerifyWebhookSignatureRequest | 

    try:
        # Verify an HMAC webhook signature
        api_response = api_instance.verify_webhook_signature(free_tool_verify_webhook_signature_request)
        print("The response of FreeToolsApi->verify_webhook_signature:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FreeToolsApi->verify_webhook_signature: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **free_tool_verify_webhook_signature_request** | [**FreeToolVerifyWebhookSignatureRequest**](FreeToolVerifyWebhookSignatureRequest.md)|  | 

### Return type

[**FreeToolVerifyWebhookSignatureResponse**](FreeToolVerifyWebhookSignatureResponse.md)

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


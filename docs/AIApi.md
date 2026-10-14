# postboost.AIApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**blog_to_social**](AIApi.md#blog_to_social) | **POST** /{workspaceUuid}/ai/blog-to-social | Generate social media captions from a blog post
[**delete_brand_voice**](AIApi.md#delete_brand_voice) | **DELETE** /{workspaceUuid}/brand-voice | Delete the brand voice
[**get_ai_usage**](AIApi.md#get_ai_usage) | **GET** /{workspaceUuid}/usage/ai | AI credit usage
[**get_brand_voice**](AIApi.md#get_brand_voice) | **GET** /{workspaceUuid}/brand-voice | Get the brand voice
[**get_repurpose_run**](AIApi.md#get_repurpose_run) | **GET** /{workspaceUuid}/ai/repurpose/runs/{runId} | Get a repurpose run
[**image_alt_text**](AIApi.md#image_alt_text) | **POST** /{workspaceUuid}/ai/image-alt-text | Generate alt text for a media image using AI
[**image_edit**](AIApi.md#image_edit) | **POST** /{workspaceUuid}/ai/image-edit | Edit an existing media image using AI
[**image_generate**](AIApi.md#image_generate) | **POST** /{workspaceUuid}/ai/image-generate | Generate social media images from a caption
[**image_prompt**](AIApi.md#image_prompt) | **POST** /{workspaceUuid}/ai/image-prompt | Build an optimized image prompt from a social media caption
[**image_variations**](AIApi.md#image_variations) | **POST** /{workspaceUuid}/ai/image-variations | Generate variations of an existing media image
[**learn_brand_voice**](AIApi.md#learn_brand_voice) | **POST** /{workspaceUuid}/brand-voice/learn | Learn a brand voice from past posts
[**repurpose_content**](AIApi.md#repurpose_content) | **POST** /{workspaceUuid}/ai/repurpose | Repurpose long-form content into a draft post set with a carousel
[**update_brand_voice**](AIApi.md#update_brand_voice) | **PUT** /{workspaceUuid}/brand-voice | Create or update the brand voice


# **blog_to_social**
> BlogToSocial200Response blog_to_social(workspace_uuid, blog_to_social_input)

Generate social media captions from a blog post

Generates platform-specific social media captions from a blog post URL or directly provided title and excerpt. Each platform generates one caption, which consumes one AI credit from the workspace's monthly allowance.  **Input modes** (at least one required): - **URL mode**: provide `url` and the API scrapes the blog content automatically, including detecting the featured image via `og:image`. - **Direct mode**: provide `title` and `excerpt` directly (no scraping).  If both are provided, direct values take priority.  When `create_post` is `true`, a draft post is created in the workspace with per-account caption versions. If an image is available (from `image_url` or the scraped `og:image`), it is imported into the workspace media library and attached to the draft post. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.blog_to_social200_response import BlogToSocial200Response
from postboost.models.blog_to_social_input import BlogToSocialInput
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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    blog_to_social_input = {"url":"https://example.com/blog/my-post","platforms":["twitter","linkedin"],"tone":"professional","hashtags":"few","create_post":false} # BlogToSocialInput | 

    try:
        # Generate social media captions from a blog post
        api_response = api_instance.blog_to_social(workspace_uuid, blog_to_social_input)
        print("The response of AIApi->blog_to_social:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->blog_to_social: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **blog_to_social_input** | [**BlogToSocialInput**](BlogToSocialInput.md)|  | 

### Return type

[**BlogToSocial200Response**](BlogToSocial200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Captions generated successfully |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |
**429** | AI credits exhausted for this billing period |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_brand_voice**
> object delete_brand_voice(workspace_uuid)

Delete the brand voice

Removes the workspace's brand voice. AI endpoints then run without one. Admins and members only.

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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # Delete the brand voice
        api_response = api_instance.delete_brand_voice(workspace_uuid)
        print("The response of AIApi->delete_brand_voice:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->delete_brand_voice: %s\n" % e)
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

# **get_ai_usage**
> AIUsage get_ai_usage(workspace_uuid)

AI credit usage

The workspace's AI credits: text credits (captions, rewrites, outlines, alt text; counted per billing cycle) and image credits (one per generated, edited or varied image, and one per repurpose carousel; counted per calendar month, UTC). `limit` and `remaining` are `null` when the workspace has no limit. Readable when credits are used up; costs nothing.  When image credits run out, the image endpoints and carousels answer `429` with `code: image_credits_exhausted`; when text credits run out, the AI endpoints answer `429` with `code: ai_credits_exhausted`. Image endpoint responses also carry `image_credits_used` and `image_credits_remaining`; their `credits_used` counts text credits only. If the image pool is switched off (`image.enabled: false`), images cost text credits as before. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.ai_usage import AIUsage
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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # AI credit usage
        api_response = api_instance.get_ai_usage(workspace_uuid)
        print("The response of AIApi->get_ai_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->get_ai_usage: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**AIUsage**](AIUsage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Credit usage |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_brand_voice**
> GetBrandVoice200Response get_brand_voice(workspace_uuid)

Get the brand voice

The workspace's brand voice: identity, audience, tone sliders, style rules and example posts. It is the same profile as the Brand Voice page in the app (one per workspace). `data` is `null` when no voice is set. Any workspace member may read it; reading costs no AI credits.  The AI endpoints apply it automatically: `blog-to-social` adds it to the caption instructions, `image-prompt` and `image-generate` turn it into a short visual tone line, and `image-edit` applies it when you send `use_brand_voice: true`. `image-variations` and `image-alt-text` never use it (alt text must describe the image literally). Send `use_brand_voice: false` to skip it on a call; responses report `meta.brand_voice_applied`. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_brand_voice200_response import GetBrandVoice200Response
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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.

    try:
        # Get the brand voice
        api_response = api_instance.get_brand_voice(workspace_uuid)
        print("The response of AIApi->get_brand_voice:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->get_brand_voice: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 

### Return type

[**GetBrandVoice200Response**](GetBrandVoice200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The brand voice, or &#x60;null&#x60; when none is set |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_repurpose_run**
> GetRepurposeRun200Response get_repurpose_run(workspace_uuid, run_id)

Get a repurpose run

Status of a run started by `repurposeContent`. `queued` and `running` mean it is still going; poll again in a few seconds. A run that has not finished after 10 minutes reports `failed`. `result` holds the same `data` body a `200` from `repurposeContent` returns, for one hour after the run ended with `ok` or `partial`; after that it is `null` (the draft post stays). Limited to 60 calls per minute. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.get_repurpose_run200_response import GetRepurposeRun200Response
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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    run_id = 56 # int | The `run_id` from `repurposeContent`.

    try:
        # Get a repurpose run
        api_response = api_instance.get_repurpose_run(workspace_uuid, run_id)
        print("The response of AIApi->get_repurpose_run:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->get_repurpose_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **run_id** | **int**| The &#x60;run_id&#x60; from &#x60;repurposeContent&#x60;. | 

### Return type

[**GetRepurposeRun200Response**](GetRepurposeRun200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Run status |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **image_alt_text**
> ImageAltText200Response image_alt_text(workspace_uuid, image_alt_text_input)

Generate alt text for a media image using AI

Analyzes an existing workspace media item and generates accessible alt text. The alt text is saved back to the media record. Costs 1 AI credit per call. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.image_alt_text200_response import ImageAltText200Response
from postboost.models.image_alt_text_input import ImageAltTextInput
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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    image_alt_text_input = postboost.ImageAltTextInput() # ImageAltTextInput | 

    try:
        # Generate alt text for a media image using AI
        api_response = api_instance.image_alt_text(workspace_uuid, image_alt_text_input)
        print("The response of AIApi->image_alt_text:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->image_alt_text: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **image_alt_text_input** | [**ImageAltTextInput**](ImageAltTextInput.md)|  | 

### Return type

[**ImageAltText200Response**](ImageAltText200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Alt text generated and saved to media record |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |
**429** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **image_edit**
> ImageGenerate200Response image_edit(workspace_uuid, image_edit_input)

Edit an existing media image using AI

Edits an existing workspace media item using the source image and a text prompt. Optionally accepts a mask (transparent areas are replaced). Saves results to the media library. Credits: `count × credit_weight`. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.image_edit_input import ImageEditInput
from postboost.models.image_generate200_response import ImageGenerate200Response
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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    image_edit_input = postboost.ImageEditInput() # ImageEditInput | 

    try:
        # Edit an existing media image using AI
        api_response = api_instance.image_edit(workspace_uuid, image_edit_input)
        print("The response of AIApi->image_edit:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->image_edit: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **image_edit_input** | [**ImageEditInput**](ImageEditInput.md)|  | 

### Return type

[**ImageGenerate200Response**](ImageGenerate200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Images edited and saved to media library |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |
**429** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **image_generate**
> ImageGenerate200Response image_generate(workspace_uuid, image_generate_input)

Generate social media images from a caption

Generates one or more images and saves them immediately to the workspace media library.  **Standard mode** (recommended): provide `caption` + `platform`. PostBoost builds a professional image prompt internally using platform-specific templates. No prompt engineering required.  **Developer mode**: provide `prompt` directly to bypass prompt building. If both `caption` and `prompt` are sent, standard mode runs.  Credits: `count x credit_weight` (default: 5 per image). 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.image_generate200_response import ImageGenerate200Response
from postboost.models.image_generate_input import ImageGenerateInput
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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    image_generate_input = {"caption":"Our summer sale starts today, 30% off everything!","platform":"instagram","template":"product_highlight","aspect_ratio":"1:1","count":2} # ImageGenerateInput | 

    try:
        # Generate social media images from a caption
        api_response = api_instance.image_generate(workspace_uuid, image_generate_input)
        print("The response of AIApi->image_generate:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->image_generate: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **image_generate_input** | [**ImageGenerateInput**](ImageGenerateInput.md)|  | 

### Return type

[**ImageGenerate200Response**](ImageGenerate200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Images generated and saved to media library |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |
**429** | AI credits exhausted for this billing period |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **image_prompt**
> ImagePrompt200Response image_prompt(workspace_uuid, image_prompt_input)

Build an optimized image prompt from a social media caption

Builds a professional image generation prompt from a caption and platform. No image is generated. Use this to preview the prompt before calling `image-generate`. Costs 1 AI credit per call.  When `image-generate` builds the prompt internally (standard mode), no credit is charged for the prompt step. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.image_prompt200_response import ImagePrompt200Response
from postboost.models.image_prompt_input import ImagePromptInput
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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    image_prompt_input = postboost.ImagePromptInput() # ImagePromptInput | 

    try:
        # Build an optimized image prompt from a social media caption
        api_response = api_instance.image_prompt(workspace_uuid, image_prompt_input)
        print("The response of AIApi->image_prompt:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->image_prompt: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **image_prompt_input** | [**ImagePromptInput**](ImagePromptInput.md)|  | 

### Return type

[**ImagePrompt200Response**](ImagePrompt200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Prompt built successfully |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |
**429** | AI credits exhausted for this billing period |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **image_variations**
> ImageVariations200Response image_variations(workspace_uuid, image_variations_input)

Generate variations of an existing media image

Creates one or more variations of an existing workspace media item. Saves results to the media library. Credits: `count × credit_weight`. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.image_variations200_response import ImageVariations200Response
from postboost.models.image_variations_input import ImageVariationsInput
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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    image_variations_input = postboost.ImageVariationsInput() # ImageVariationsInput | 

    try:
        # Generate variations of an existing media image
        api_response = api_instance.image_variations(workspace_uuid, image_variations_input)
        print("The response of AIApi->image_variations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->image_variations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **image_variations_input** | [**ImageVariationsInput**](ImageVariationsInput.md)|  | 

### Return type

[**ImageVariations200Response**](ImageVariations200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Variations generated and saved to media library |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |
**429** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **learn_brand_voice**
> LearnBrandVoiceResponse learn_brand_voice(workspace_uuid, learn_brand_voice_input=learn_brand_voice_input)

Learn a brand voice from past posts

Reads the workspace's latest published posts (original text) and proposes a brand voice in the same shape as `GET /brand-voice`. Returns a draft and saves nothing unless `apply: true`.  Without `overwrite`, learned values only fill fields that are empty (tone sliders and styles still at their defaults count as empty); with `overwrite: true` they replace them. The first five sampled posts become `example_posts`. Needs at least 3 published posts (`422`, `code: not_enough_posts`). Costs one AI text credit per AI call (one retry when the reply is not usable). Admins and members only. A key limited to some accounts must send `account_ids`; only posts whose accounts are all among them are read. `apply` also needs the `write` ability. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.learn_brand_voice_input import LearnBrandVoiceInput
from postboost.models.learn_brand_voice_response import LearnBrandVoiceResponse
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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    learn_brand_voice_input = postboost.LearnBrandVoiceInput() # LearnBrandVoiceInput |  (optional)

    try:
        # Learn a brand voice from past posts
        api_response = api_instance.learn_brand_voice(workspace_uuid, learn_brand_voice_input=learn_brand_voice_input)
        print("The response of AIApi->learn_brand_voice:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->learn_brand_voice: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **learn_brand_voice_input** | [**LearnBrandVoiceInput**](LearnBrandVoiceInput.md)|  | [optional] 

### Return type

[**LearnBrandVoiceResponse**](LearnBrandVoiceResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Proposed (or saved) brand voice |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** | Validation error, AI disabled, or fewer than 3 published posts (&#x60;code: not_enough_posts&#x60;) |  -  |
**429** | AI text credits used up (&#x60;code: ai_credits_exhausted&#x60;) |  -  |
**502** | The AI reply was not a usable profile (&#x60;code: ai_unusable_response&#x60;) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **repurpose_content**
> RepurposeContent200Response repurpose_content(workspace_uuid, repurpose_input, idempotency_key=idempotency_key)

Repurpose long-form content into a draft post set with a carousel

Turns an article URL, a YouTube video, a PDF or pasted text into one **draft** post with a caption for every target account, plus a carousel of rendered slide images (hook, 1 to 6 idea slides, call to action; 1080×1350 PNG). Nothing is published or scheduled.  **Sources** (`source_type`): - `url`: the article is fetched and its main text extracted. - `youtube`: title, description and chapters come from YouTube; send the transcript in   `transcript` for better results (required when the description is short). - `pdf`: `pdf_url` must be a public PDF of at most 20 MB; the first 30 pages are read. - `text`: send `title` and `text`.  **Carousel per network**: Instagram, Facebook, Threads up to 10 slides; LinkedIn up to 9; X and Bluesky up to 4; other networks get the cover slide; YouTube and TikTok get none (listed in `warnings`). Without a carousel, the source image (article image or video thumbnail) is attached when available.  **AI credits**: one per target account plus one for the carousel outline. Slides are drawn without AI and cost nothing. The workspace brand voice applies unless `use_brand_voice` is `false`. Send an `Idempotency-Key` so a retried call does not create a second draft. Limited to 10 calls per minute.  **Long runs**: the run is queued. The call waits up to 20 seconds and answers `200` with the result when the run finished by then. Otherwise it answers `202` with a `run_id`; poll `getRepurposeRun` (`status_url`) every few seconds until the status is `ok`, `partial` or `failed`. Send `async: true` to get the `202` right away. Validation, account and credit errors are answered before anything is queued. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.repurpose_content200_response import RepurposeContent200Response
from postboost.models.repurpose_input import RepurposeInput
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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    repurpose_input = {"source_type":"url","url":"https://example.com/blog/my-post","platforms":["instagram","linkedin_page"],"slide_count":7} # RepurposeInput | 
    idempotency_key = 'idempotency_key_example' # str | Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with `Idempotent-Replayed: true` and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  (optional)

    try:
        # Repurpose long-form content into a draft post set with a carousel
        api_response = api_instance.repurpose_content(workspace_uuid, repurpose_input, idempotency_key=idempotency_key)
        print("The response of AIApi->repurpose_content:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->repurpose_content: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **repurpose_input** | [**RepurposeInput**](RepurposeInput.md)|  | 
 **idempotency_key** | **str**| Unique key (for example a UUID) that makes the request safe to retry. A repeat with the same key and body within 24 hours returns the stored response with &#x60;Idempotent-Replayed: true&#x60; and has no further effect. Keys are scoped to your user, the workspace, the method and the path.  | [optional] 

### Return type

[**RepurposeContent200Response**](RepurposeContent200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Draft post set created |  -  |
**202** | The run is still going (or &#x60;async&#x60; was set); poll &#x60;status_url&#x60;. |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |
**429** |  |  -  |
**500** | The run failed while the call waited. &#x60;getRepurposeRun&#x60; shows the error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_brand_voice**
> GetBrandVoice200Response update_brand_voice(workspace_uuid, brand_voice_input)

Create or update the brand voice

Creates the workspace's brand voice or updates it. Fields you leave out keep their current value. Admins and members only (not viewers); the workspace must have AI enabled. 

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.brand_voice_input import BrandVoiceInput
from postboost.models.get_brand_voice200_response import GetBrandVoice200Response
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
    api_instance = postboost.AIApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str | UUID of the workspace.
    brand_voice_input = {"business_name":"Northwind Coffee","industry":"Specialty coffee roasting","personality":"Warm and curious about every bean. Never pushy.","audience":["home baristas","cafe owners"],"tone_formal":2,"tone_playful":4,"tone_technical":3,"emoji_style":"rare","hashtag_strategy":"branded","avoid_words":["cheap","best ever"]} # BrandVoiceInput | 

    try:
        # Create or update the brand voice
        api_response = api_instance.update_brand_voice(workspace_uuid, brand_voice_input)
        print("The response of AIApi->update_brand_voice:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIApi->update_brand_voice: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**| UUID of the workspace. | 
 **brand_voice_input** | [**BrandVoiceInput**](BrandVoiceInput.md)|  | 

### Return type

[**GetBrandVoice200Response**](GetBrandVoice200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The saved brand voice |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


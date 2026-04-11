# postboost.AIApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**blog_to_social**](AIApi.md#blog_to_social) | **POST** /{workspaceUuid}/ai/blog-to-social | Generate social media captions from a blog post
[**image_alt_text**](AIApi.md#image_alt_text) | **POST** /{workspaceUuid}/ai/image-alt-text | Generate alt text for a media image using AI
[**image_edit**](AIApi.md#image_edit) | **POST** /{workspaceUuid}/ai/image-edit | Edit an existing media image using AI
[**image_generate**](AIApi.md#image_generate) | **POST** /{workspaceUuid}/ai/image-generate | Generate social media images from a caption
[**image_prompt**](AIApi.md#image_prompt) | **POST** /{workspaceUuid}/ai/image-prompt | Build an optimized image prompt from a social media caption
[**image_variations**](AIApi.md#image_variations) | **POST** /{workspaceUuid}/ai/image-variations | Generate variations of an existing media image


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
**422** |  |  -  |
**429** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


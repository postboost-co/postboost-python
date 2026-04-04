# postboost.AIApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**blog_to_social**](AIApi.md#blog_to_social) | **POST** /{workspaceUuid}/ai/blog-to-social | Generate social media captions from a blog post


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
    blog_to_social_input = {"url":"https://example.com/blog/my-post","platforms":["x","linkedin"],"tone":"professional","hashtags":"few","create_post":false} # BlogToSocialInput | 

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


# postboost.ReceiptsApi

All URIs are relative to *https://postboost.co/app/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_receipt**](ReceiptsApi.md#create_receipt) | **POST** /panel/receipts | Create receipt
[**delete_receipt**](ReceiptsApi.md#delete_receipt) | **DELETE** /panel/receipts/{receiptUuid} | Delete receipt
[**delete_receipts_bulk**](ReceiptsApi.md#delete_receipts_bulk) | **DELETE** /panel/receipts | Delete receipts (bulk)
[**get_receipt**](ReceiptsApi.md#get_receipt) | **GET** /panel/receipts/{receiptUuid} | Get receipt
[**list_receipts**](ReceiptsApi.md#list_receipts) | **GET** /panel/receipts | List receipts
[**update_receipt**](ReceiptsApi.md#update_receipt) | **PUT** /panel/receipts/{receiptUuid} | Update receipt


# **create_receipt**
> Receipt create_receipt(receipt_input)

Create receipt

Creates a billing receipt record for a workspace. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.receipt import Receipt
from postboost.models.receipt_input import ReceiptInput
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
    api_instance = postboost.ReceiptsApi(api_client)
    receipt_input = postboost.ReceiptInput() # ReceiptInput | 

    try:
        # Create receipt
        api_response = api_instance.create_receipt(receipt_input)
        print("The response of ReceiptsApi->create_receipt:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ReceiptsApi->create_receipt: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **receipt_input** | [**ReceiptInput**](ReceiptInput.md)|  | 

### Return type

[**Receipt**](Receipt.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created receipt |  -  |
**401** |  |  -  |
**403** |  |  -  |
**422** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_receipt**
> object delete_receipt(receipt_uuid)

Delete receipt

Permanently deletes a single receipt. Admin only.

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
    api_instance = postboost.ReceiptsApi(api_client)
    receipt_uuid = 'receipt_uuid_example' # str | UUID of the receipt.

    try:
        # Delete receipt
        api_response = api_instance.delete_receipt(receipt_uuid)
        print("The response of ReceiptsApi->delete_receipt:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ReceiptsApi->delete_receipt: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **receipt_uuid** | **str**| UUID of the receipt. | 

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

# **delete_receipts_bulk**
> object delete_receipts_bulk(delete_receipts_bulk_request)

Delete receipts (bulk)

Permanently deletes one or more receipt records. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.delete_receipts_bulk_request import DeleteReceiptsBulkRequest
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
    api_instance = postboost.ReceiptsApi(api_client)
    delete_receipts_bulk_request = postboost.DeleteReceiptsBulkRequest() # DeleteReceiptsBulkRequest | 

    try:
        # Delete receipts (bulk)
        api_response = api_instance.delete_receipts_bulk(delete_receipts_bulk_request)
        print("The response of ReceiptsApi->delete_receipts_bulk:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ReceiptsApi->delete_receipts_bulk: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delete_receipts_bulk_request** | [**DeleteReceiptsBulkRequest**](DeleteReceiptsBulkRequest.md)|  | 

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

# **get_receipt**
> Receipt get_receipt(receipt_uuid)

Get receipt

Returns a single receipt by UUID. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.receipt import Receipt
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
    api_instance = postboost.ReceiptsApi(api_client)
    receipt_uuid = 'receipt_uuid_example' # str | UUID of the receipt.

    try:
        # Get receipt
        api_response = api_instance.get_receipt(receipt_uuid)
        print("The response of ReceiptsApi->get_receipt:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ReceiptsApi->get_receipt: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **receipt_uuid** | **str**| UUID of the receipt. | 

### Return type

[**Receipt**](Receipt.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Receipt details |  -  |
**401** |  |  -  |
**403** |  |  -  |
**404** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_receipts**
> ListReceipts200Response list_receipts(workspace_uuid=workspace_uuid, invoice_number=invoice_number, page=page)

List receipts

Returns a paginated list of billing receipts. Filter by workspace UUID or invoice number. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.list_receipts200_response import ListReceipts200Response
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
    api_instance = postboost.ReceiptsApi(api_client)
    workspace_uuid = 'workspace_uuid_example' # str |  (optional)
    invoice_number = 'invoice_number_example' # str |  (optional)
    page = 1 # int | Page number (15 items per page). (optional) (default to 1)

    try:
        # List receipts
        api_response = api_instance.list_receipts(workspace_uuid=workspace_uuid, invoice_number=invoice_number, page=page)
        print("The response of ReceiptsApi->list_receipts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ReceiptsApi->list_receipts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_uuid** | **str**|  | [optional] 
 **invoice_number** | **str**|  | [optional] 
 **page** | **int**| Page number (15 items per page). | [optional] [default to 1]

### Return type

[**ListReceipts200Response**](ListReceipts200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Paginated list of receipts |  -  |
**401** |  |  -  |
**403** |  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_receipt**
> object update_receipt(receipt_uuid, receipt_update_input)

Update receipt

Updates a receipt's transaction details, amount, or payment date. Admin only.

### Example

* Bearer Authentication (bearerAuth):

```python
import postboost
from postboost.models.receipt_update_input import ReceiptUpdateInput
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
    api_instance = postboost.ReceiptsApi(api_client)
    receipt_uuid = 'receipt_uuid_example' # str | UUID of the receipt.
    receipt_update_input = postboost.ReceiptUpdateInput() # ReceiptUpdateInput | 

    try:
        # Update receipt
        api_response = api_instance.update_receipt(receipt_uuid, receipt_update_input)
        print("The response of ReceiptsApi->update_receipt:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ReceiptsApi->update_receipt: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **receipt_uuid** | **str**| UUID of the receipt. | 
 **receipt_update_input** | [**ReceiptUpdateInput**](ReceiptUpdateInput.md)|  | 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


# RetryPostAccountResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**status** | [**PostStatus**](PostStatus.md) |  | 
**publish_progress** | [**PublishProgress**](PublishProgress.md) |  | 

## Example

```python
from postboost.models.retry_post_account_result import RetryPostAccountResult

# TODO update the JSON string below
json = "{}"
# create an instance of RetryPostAccountResult from a JSON string
retry_post_account_result_instance = RetryPostAccountResult.from_json(json)
# print the JSON string representation of the object
print(RetryPostAccountResult.to_json())

# convert the object into a dict
retry_post_account_result_dict = retry_post_account_result_instance.to_dict()
# create an instance of RetryPostAccountResult from a dict
retry_post_account_result_from_dict = RetryPostAccountResult.from_dict(retry_post_account_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



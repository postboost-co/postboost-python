# FreeToolGetGlossaryResponseTermsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**term** | **str** | The term. | [optional] 
**slug** | **str** | Stable key of the term, also its anchor on the page. | [optional] 
**category** | **str** | Category. | [optional] 
**definition** | **str** | Plain-language definition in one to three sentences. | [optional] 
**networks** | **List[str]** | Networks the term is specific to (provider keys); empty when it applies to all. | [optional] 
**related** | **List[str]** | Slugs of related terms. | [optional] 
**url** | **str** | The term on the glossary page. | [optional] 
**learn_url** | **str** | A PostBoost guide that goes deeper, or null. | [optional] 
**tool_url** | **str** | A free tool for the job, or null. | [optional] 
**feature_url** | **str** | The PostBoost feature page, or null. | [optional] 
**source** | **str** | Where a platform rule or number in the definition comes from, or null. | [optional] 

## Example

```python
from postboost.models.free_tool_get_glossary_response_terms_inner import FreeToolGetGlossaryResponseTermsInner

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolGetGlossaryResponseTermsInner from a JSON string
free_tool_get_glossary_response_terms_inner_instance = FreeToolGetGlossaryResponseTermsInner.from_json(json)
# print the JSON string representation of the object
print(FreeToolGetGlossaryResponseTermsInner.to_json())

# convert the object into a dict
free_tool_get_glossary_response_terms_inner_dict = free_tool_get_glossary_response_terms_inner_instance.to_dict()
# create an instance of FreeToolGetGlossaryResponseTermsInner from a dict
free_tool_get_glossary_response_terms_inner_from_dict = FreeToolGetGlossaryResponseTermsInner.from_dict(free_tool_get_glossary_response_terms_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



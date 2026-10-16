# FreeToolCheckReadabilityResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**supported** | **bool** | False for a language other than English: no scores, hints or suggestions. | [optional] 
**note** | **str** | Why the text was not scored, or null. | [optional] 
**flesch_reading_ease** | **float** | Flesch reading ease, one decimal: higher is easier, 60-70 is plain English. Null when not scored. | [optional] 
**flesch_kincaid_grade** | **float** | Flesch-Kincaid grade level, one decimal: the US school grade that can read the text. Null when not scored. | [optional] 
**sentences** | **int** | Sentences with at least one word. | [optional] 
**words** | **int** | Words, not counting hashtags, @mentions, links and emoji. | [optional] 
**syllables** | **int** | Syllables, by the heuristic described in the docs. | [optional] 
**avg_words_per_sentence** | **float** | Words per sentence, one decimal. | [optional] 
**long_sentences** | [**List[FreeToolCheckReadabilityResponseLongSentencesInner]**](FreeToolCheckReadabilityResponseLongSentencesInner.md) | Sentences of more than 25 words. | [optional] 
**passive_hints** | **int** | Possible passive phrases (\&quot;was written\&quot;, \&quot;is being reviewed\&quot;). A hint, not a grammar check. | [optional] 
**emoji_count** | **int** | Emoji (Extended_Pictographic characters). | [optional] 
**hashtag_count** | **int** | Hashtags. | [optional] 
**suggestions** | **List[str]** | Plain fixes, e.g. which sentence to split. Empty when the text reads easily. | [optional] 

## Example

```python
from postboost.models.free_tool_check_readability_response import FreeToolCheckReadabilityResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FreeToolCheckReadabilityResponse from a JSON string
free_tool_check_readability_response_instance = FreeToolCheckReadabilityResponse.from_json(json)
# print the JSON string representation of the object
print(FreeToolCheckReadabilityResponse.to_json())

# convert the object into a dict
free_tool_check_readability_response_dict = free_tool_check_readability_response_instance.to_dict()
# create an instance of FreeToolCheckReadabilityResponse from a dict
free_tool_check_readability_response_from_dict = FreeToolCheckReadabilityResponse.from_dict(free_tool_check_readability_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



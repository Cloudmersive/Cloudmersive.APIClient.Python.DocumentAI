# cloudmersive_documentai_api_client.AnalyzeApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**answer_questions**](AnalyzeApi.md#answer_questions) | **POST** /document-ai/document/analyze/answer-questions | Answer Questions about a Document in a structured way using Advanced AI
[**apply_rules**](AnalyzeApi.md#apply_rules) | **POST** /document-ai/document/analyze/enforce-policy | Enforce Policies to a Document to allow or block it using Advanced AI


# **answer_questions**
> DocumentQuestionAnswersResult answer_questions(body=body)

Answer Questions about a Document in a structured way using Advanced AI

Answer boolean (yes/no), multiple-choice and free-response questions about the contents of a document using Advanced AI.  Input document formats supported include DOCX, PDF, PNG and JPG.  Consumes 100 API calls per page.

### Example
```python
from __future__ import print_function
import time
import cloudmersive_documentai_api_client
from cloudmersive_documentai_api_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Apikey
configuration = cloudmersive_documentai_api_client.Configuration()
configuration.api_key['Apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Apikey'] = 'Bearer'

# create an instance of the API class
api_instance = cloudmersive_documentai_api_client.AnalyzeApi(cloudmersive_documentai_api_client.ApiClient(configuration))
body = cloudmersive_documentai_api_client.DocumentQuestionsRequest() # DocumentQuestionsRequest | Input request, including document and questions (optional)

try:
    # Answer Questions about a Document in a structured way using Advanced AI
    api_response = api_instance.answer_questions(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling AnalyzeApi->answer_questions: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DocumentQuestionsRequest**](DocumentQuestionsRequest.md)| Input request, including document and questions | [optional] 

### Return type

[**DocumentQuestionAnswersResult**](DocumentQuestionAnswersResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **apply_rules**
> DocumentPolicyResult apply_rules(body=body)

Enforce Policies to a Document to allow or block it using Advanced AI

Enforce Policies to a Document to allow or block it using Advanced AI.  Input document formats supported include DOCX, PDF, PNG and JPG.  Consumes 100 API calls per page.

### Example
```python
from __future__ import print_function
import time
import cloudmersive_documentai_api_client
from cloudmersive_documentai_api_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Apikey
configuration = cloudmersive_documentai_api_client.Configuration()
configuration.api_key['Apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Apikey'] = 'Bearer'

# create an instance of the API class
api_instance = cloudmersive_documentai_api_client.AnalyzeApi(cloudmersive_documentai_api_client.ApiClient(configuration))
body = cloudmersive_documentai_api_client.DocumentPolicyRequest() # DocumentPolicyRequest | Input request, including document and policy rules (optional)

try:
    # Enforce Policies to a Document to allow or block it using Advanced AI
    api_response = api_instance.apply_rules(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling AnalyzeApi->apply_rules: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**DocumentPolicyRequest**](DocumentPolicyRequest.md)| Input request, including document and policy rules | [optional] 

### Return type

[**DocumentPolicyResult**](DocumentPolicyResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


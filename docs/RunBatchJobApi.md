# cloudmersive_documentai_api_client.RunBatchJobApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**extract_all_fields_and_tables_from_document_batch_job**](RunBatchJobApi.md#extract_all_fields_and_tables_from_document_batch_job) | **POST** /document-ai/document/batch-job/extract/all | Extract All Fields and Tables of Data from a Document using AI as a Batch Job
[**extract_classification_from_document_batch_job**](RunBatchJobApi.md#extract_classification_from_document_batch_job) | **POST** /document-ai/document/batch-job/extract/classify | Extract Classification or Category from a Document using AI as a Batch Job
[**extract_fields_from_document_advanced_batch_job**](RunBatchJobApi.md#extract_fields_from_document_advanced_batch_job) | **POST** /document-ai/document/batch-job/extract/fields/advanced | Extract Field Values from a Document using Advanced AI as a Batch Job
[**extract_text_from_document_batch_job**](RunBatchJobApi.md#extract_text_from_document_batch_job) | **POST** /document-ai/document/batch-job/extract/text | Extract Text from a Document using AI as a Batch Job
[**get_async_job_status**](RunBatchJobApi.md#get_async_job_status) | **GET** /document-ai/document/batch-job/batch-job/status | Get the status and result of an Extract Document Batch Job


# **extract_all_fields_and_tables_from_document_batch_job**
> ExtractDocumentBatchJobResult extract_all_fields_and_tables_from_document_batch_job(recognition_mode=recognition_mode, input_file=input_file)

Extract All Fields and Tables of Data from a Document using AI as a Batch Job

Creates an async batch job for processing a large document as an AI batch job.  Extract all Fields and Tables, comprised of rows and columns of data, from a document using AI.  Input document formats supported include DOCX, PDF, PNG and JPG.  Requires Managed Instance or Private Cloud deployment.

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
api_instance = cloudmersive_documentai_api_client.RunBatchJobApi(cloudmersive_documentai_api_client.ApiClient(configuration))
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
input_file = '/path/to/file.txt' # file | Input document, or photos of a document, to extract data from (optional)

try:
    # Extract All Fields and Tables of Data from a Document using AI as a Batch Job
    api_response = api_instance.extract_all_fields_and_tables_from_document_batch_job(recognition_mode=recognition_mode, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RunBatchJobApi->extract_all_fields_and_tables_from_document_batch_job: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **file**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractDocumentBatchJobResult**](ExtractDocumentBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extract_classification_from_document_batch_job**
> ExtractDocumentBatchJobResult extract_classification_from_document_batch_job(categories=categories, recognition_mode=recognition_mode, input_file=input_file)

Extract Classification or Category from a Document using AI as a Batch Job

Creates an async batch job for processing a large document as an AI batch job.  Extract Classification or Category (e.g. Invoice, Receipt, Tax Form, or Form 1040, Form 1040 EZ, etc.) from a document using AI.  Input document formats supported include DOCX, PDF, PNG and JPG.  Requires Managed Instance or Private Cloud deployment.

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
api_instance = cloudmersive_documentai_api_client.RunBatchJobApi(cloudmersive_documentai_api_client.ApiClient(configuration))
categories = 'categories_example' # str | Desired classification to extract (optional)
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
input_file = '/path/to/file.txt' # file | Input document, or photos of a document, to extract data from (optional)

try:
    # Extract Classification or Category from a Document using AI as a Batch Job
    api_response = api_instance.extract_classification_from_document_batch_job(categories=categories, recognition_mode=recognition_mode, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RunBatchJobApi->extract_classification_from_document_batch_job: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **categories** | **str**| Desired classification to extract | [optional] 
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **file**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractDocumentBatchJobResult**](ExtractDocumentBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extract_fields_from_document_advanced_batch_job**
> ExtractDocumentBatchJobResult extract_fields_from_document_advanced_batch_job(recognition_mode=recognition_mode, body=body)

Extract Field Values from a Document using Advanced AI as a Batch Job

Creates an async batch job for processing a large document as an AI batch job.  Extract Field Values (e.g. Invoice Number, Invoice Date, Business Card Phone Number, etc.) from a document using Advanced AI.  Input document formats supported include DOCX, PDF, PNG and JPG.  Requires Managed Instance or Private Cloud deployment.

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
api_instance = cloudmersive_documentai_api_client.RunBatchJobApi(cloudmersive_documentai_api_client.ApiClient(configuration))
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
body = cloudmersive_documentai_api_client.AdvancedExtractFieldsRequest() # AdvancedExtractFieldsRequest |  (optional)

try:
    # Extract Field Values from a Document using Advanced AI as a Batch Job
    api_response = api_instance.extract_fields_from_document_advanced_batch_job(recognition_mode=recognition_mode, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RunBatchJobApi->extract_fields_from_document_advanced_batch_job: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **body** | [**AdvancedExtractFieldsRequest**](AdvancedExtractFieldsRequest.md)|  | [optional] 

### Return type

[**ExtractDocumentBatchJobResult**](ExtractDocumentBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extract_text_from_document_batch_job**
> ExtractDocumentBatchJobResult extract_text_from_document_batch_job(recognition_mode=recognition_mode, input_file=input_file)

Extract Text from a Document using AI as a Batch Job

Creates an async batch job for processing a large document as an AI batch job.  Input document formats supported include DOCX, PDF, PNG and JPG.  Supports a wide range of languages.  Requires Managed Instance or Private Cloud deployment.

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
api_instance = cloudmersive_documentai_api_client.RunBatchJobApi(cloudmersive_documentai_api_client.ApiClient(configuration))
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
input_file = '/path/to/file.txt' # file | Input document, or photos of a document, to extract data from (optional)

try:
    # Extract Text from a Document using AI as a Batch Job
    api_response = api_instance.extract_text_from_document_batch_job(recognition_mode=recognition_mode, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RunBatchJobApi->extract_text_from_document_batch_job: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **file**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractDocumentBatchJobResult**](ExtractDocumentBatchJobResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_async_job_status**
> ExtractDocumentJobStatusResult get_async_job_status(async_job_id=async_job_id)

Get the status and result of an Extract Document Batch Job

Returns the result of the Async Job - possible states can be STARTED or COMPLETED.  This API is only available for Cloudmersive Managed Instance and Private Cloud deployments.

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
api_instance = cloudmersive_documentai_api_client.RunBatchJobApi(cloudmersive_documentai_api_client.ApiClient(configuration))
async_job_id = 'async_job_id_example' # str |  (optional)

try:
    # Get the status and result of an Extract Document Batch Job
    api_response = api_instance.get_async_job_status(async_job_id=async_job_id)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling RunBatchJobApi->get_async_job_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **async_job_id** | **str**|  | [optional] 

### Return type

[**ExtractDocumentJobStatusResult**](ExtractDocumentJobStatusResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


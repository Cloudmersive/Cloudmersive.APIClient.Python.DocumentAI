# cloudmersive_documentai_api_client.ExtractApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**extract_all_fields_and_tables**](ExtractApi.md#extract_all_fields_and_tables) | **POST** /document-ai/document/extract/all | Extract All Fields and Tables of Data from a Document using AI
[**extract_barcodes**](ExtractApi.md#extract_barcodes) | **POST** /document-ai/document/extract/barcodes | Extract Barcodes of from a Document using AI
[**extract_classification**](ExtractApi.md#extract_classification) | **POST** /document-ai/document/extract/classify | Extract Classification or Category from a Document using AI
[**extract_classification_advanced**](ExtractApi.md#extract_classification_advanced) | **POST** /document-ai/document/extract/classify/advanced | Extract Classification or Category from a Document using Advanced AI
[**extract_fields**](ExtractApi.md#extract_fields) | **POST** /document-ai/document/extract/fields | Extract Field Values from a Document using AI
[**extract_fields_advanced**](ExtractApi.md#extract_fields_advanced) | **POST** /document-ai/document/extract/fields/advanced | Extract Field Values from a Document using Advanced AI
[**extract_summary**](ExtractApi.md#extract_summary) | **POST** /document-ai/document/extract/summary | Extract Summary from a Document using AI
[**extract_tables**](ExtractApi.md#extract_tables) | **POST** /document-ai/document/extract/tables | Extract Tables of Data from a Document using AI
[**extract_text**](ExtractApi.md#extract_text) | **POST** /document-ai/document/extract/text | Extract Text from a Document using AI


# **extract_all_fields_and_tables**
> ExtractFieldsAndTablesResponse extract_all_fields_and_tables(recognition_mode=recognition_mode, preprocessing=preprocessing, input_file=input_file)

Extract All Fields and Tables of Data from a Document using AI

Extract all Fields and Tables, comprised of rows and columns of data, from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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
api_instance = cloudmersive_documentai_api_client.ExtractApi(cloudmersive_documentai_api_client.ApiClient(configuration))
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
preprocessing = 'preprocessing_example' # str | Optional: Set the level of image pre-processing to enhance accuracy.  Possible values are 'Auto' (default), 'Paged', and 'Compatability'.  Use 'Paged' to treat each page as a separate document for extraction (requires Advanced recognitionMode).  Default is Auto. (optional)
input_file = '/path/to/file.txt' # file | Input document, or photos of a document, to extract data from (optional)

try:
    # Extract All Fields and Tables of Data from a Document using AI
    api_response = api_instance.extract_all_fields_and_tables(recognition_mode=recognition_mode, preprocessing=preprocessing, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExtractApi->extract_all_fields_and_tables: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **preprocessing** | **str**| Optional: Set the level of image pre-processing to enhance accuracy.  Possible values are &#39;Auto&#39; (default), &#39;Paged&#39;, and &#39;Compatability&#39;.  Use &#39;Paged&#39; to treat each page as a separate document for extraction (requires Advanced recognitionMode).  Default is Auto. | [optional] 
 **input_file** | **file**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractFieldsAndTablesResponse**](ExtractFieldsAndTablesResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extract_barcodes**
> ExtractBarcodesAiResponse extract_barcodes(recognition_mode=recognition_mode, input_file=input_file)

Extract Barcodes of from a Document using AI

Extract all barcodes from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG, HEIC and WEBP.  Consumes 100 API calls per page.

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
api_instance = cloudmersive_documentai_api_client.ExtractApi(cloudmersive_documentai_api_client.ApiClient(configuration))
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
input_file = '/path/to/file.txt' # file | Input document, or photos of a document, to extract data from (optional)

try:
    # Extract Barcodes of from a Document using AI
    api_response = api_instance.extract_barcodes(recognition_mode=recognition_mode, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExtractApi->extract_barcodes: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **file**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractBarcodesAiResponse**](ExtractBarcodesAiResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extract_classification**
> DocumentClassificationResult extract_classification(categories=categories, recognition_mode=recognition_mode, input_file=input_file)

Extract Classification or Category from a Document using AI

Extract Classification or Category (e.g. Invoice, Receipt, Tax Form, or Form 1040, Form 1040 EZ, etc.) from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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
api_instance = cloudmersive_documentai_api_client.ExtractApi(cloudmersive_documentai_api_client.ApiClient(configuration))
categories = 'categories_example' # str | Desired classification to extract (optional)
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
input_file = '/path/to/file.txt' # file | Input document, or photos of a document, to extract data from (optional)

try:
    # Extract Classification or Category from a Document using AI
    api_response = api_instance.extract_classification(categories=categories, recognition_mode=recognition_mode, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExtractApi->extract_classification: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **categories** | **str**| Desired classification to extract | [optional] 
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **file**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**DocumentClassificationResult**](DocumentClassificationResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extract_classification_advanced**
> DocumentAdvancedClassificationResult extract_classification_advanced(recognition_mode=recognition_mode, body=body)

Extract Classification or Category from a Document using Advanced AI

Extract Classification or Category (e.g. Invoice, Receipt, Tax Form, or Form 1040, Form 1040 EZ, etc.) from a document using Advanced AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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
api_instance = cloudmersive_documentai_api_client.ExtractApi(cloudmersive_documentai_api_client.ApiClient(configuration))
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
body = cloudmersive_documentai_api_client.AdvancedExtractClassificationRequest() # AdvancedExtractClassificationRequest | Input request to perform the classification on (optional)

try:
    # Extract Classification or Category from a Document using Advanced AI
    api_response = api_instance.extract_classification_advanced(recognition_mode=recognition_mode, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExtractApi->extract_classification_advanced: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **body** | [**AdvancedExtractClassificationRequest**](AdvancedExtractClassificationRequest.md)| Input request to perform the classification on | [optional] 

### Return type

[**DocumentAdvancedClassificationResult**](DocumentAdvancedClassificationResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extract_fields**
> ExtractFieldsResponse extract_fields(field_names=field_names, recognition_mode=recognition_mode, input_file=input_file)

Extract Field Values from a Document using AI

Extract Field Values (e.g. Invoice Number, Invoice Date, Business Card Phone Number, etc.) from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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
api_instance = cloudmersive_documentai_api_client.ExtractApi(cloudmersive_documentai_api_client.ApiClient(configuration))
field_names = 'field_names_example' # str | Desired fields to extract, comma separated (optional)
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
input_file = '/path/to/file.txt' # file | Input document, or photos of a document, to extract data from (optional)

try:
    # Extract Field Values from a Document using AI
    api_response = api_instance.extract_fields(field_names=field_names, recognition_mode=recognition_mode, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExtractApi->extract_fields: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **field_names** | **str**| Desired fields to extract, comma separated | [optional] 
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **file**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractFieldsResponse**](ExtractFieldsResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extract_fields_advanced**
> ExtractFieldsAdvancedResponse extract_fields_advanced(recognition_mode=recognition_mode, body=body)

Extract Field Values from a Document using Advanced AI

Extract Field Values (e.g. Invoice Number, Invoice Date, Business Card Phone Number, etc.) from a document using Advanced AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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
api_instance = cloudmersive_documentai_api_client.ExtractApi(cloudmersive_documentai_api_client.ApiClient(configuration))
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
body = cloudmersive_documentai_api_client.AdvancedExtractFieldsRequest() # AdvancedExtractFieldsRequest | Input request, including document file as byte array, and information on which fields to extract (optional)

try:
    # Extract Field Values from a Document using Advanced AI
    api_response = api_instance.extract_fields_advanced(recognition_mode=recognition_mode, body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExtractApi->extract_fields_advanced: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **body** | [**AdvancedExtractFieldsRequest**](AdvancedExtractFieldsRequest.md)| Input request, including document file as byte array, and information on which fields to extract | [optional] 

### Return type

[**ExtractFieldsAdvancedResponse**](ExtractFieldsAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extract_summary**
> SummarizeDocumentResponse extract_summary(recognition_mode=recognition_mode, input_file=input_file)

Extract Summary from a Document using AI

Creates a 1 paragraph summary of the input document using Artificial Intelligence.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumes 100 API calls per page.

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
api_instance = cloudmersive_documentai_api_client.ExtractApi(cloudmersive_documentai_api_client.ApiClient(configuration))
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
input_file = '/path/to/file.txt' # file | Input document, or photos of a document, to extract data from (optional)

try:
    # Extract Summary from a Document using AI
    api_response = api_instance.extract_summary(recognition_mode=recognition_mode, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExtractApi->extract_summary: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **file**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**SummarizeDocumentResponse**](SummarizeDocumentResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extract_tables**
> ExtractTablesResponse extract_tables(recognition_mode=recognition_mode, input_file=input_file)

Extract Tables of Data from a Document using AI

Extract Tables, comprised of rows and columns of data, from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Consumeds 100 API calls per page.

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
api_instance = cloudmersive_documentai_api_client.ExtractApi(cloudmersive_documentai_api_client.ApiClient(configuration))
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
input_file = '/path/to/file.txt' # file | Input document, or photos of a document, to extract data from (optional)

try:
    # Extract Tables of Data from a Document using AI
    api_response = api_instance.extract_tables(recognition_mode=recognition_mode, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExtractApi->extract_tables: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **file**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractTablesResponse**](ExtractTablesResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extract_text**
> ExtractTextResponse extract_text(recognition_mode=recognition_mode, input_file=input_file)

Extract Text from a Document using AI

Extract raw text from a document using AI.  Input document formats supported include DOCX, PDF, XLSX, PPTX, EML, MSG, JPG, PNG and WEBP.  Supports a wide range of languages.  Consumes 100 API calls per page.

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
api_instance = cloudmersive_documentai_api_client.ExtractApi(cloudmersive_documentai_api_client.ApiClient(configuration))
recognition_mode = 'recognition_mode_example' # str | Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images (optional)
input_file = '/path/to/file.txt' # file | Input document, or photos of a document, to extract data from (optional)

try:
    # Extract Text from a Document using AI
    api_response = api_instance.extract_text(recognition_mode=recognition_mode, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling ExtractApi->extract_text: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **recognition_mode** | **str**| Optional; Recognition mode - Advanced (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 
 **input_file** | **file**| Input document, or photos of a document, to extract data from | [optional] 

### Return type

[**ExtractTextResponse**](ExtractTextResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


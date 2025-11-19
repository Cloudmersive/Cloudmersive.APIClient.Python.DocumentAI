# cloudmersive_documentai_api_client
Use next-generation AI to extract data, fields, insights and text from documents. Instantly.

This Python package provides a native API client for [Cloudmersive Document AI API](https://cloudmersive.com/document-ai-api)

- API version: v1
- Package version: 3.0.4
- Build package: io.swagger.codegen.languages.PythonClientCodegen

## Requirements.

Python 2.7 and 3.4+

## Installation & Usage
### pip install

If the python package is hosted on Github, you can install directly from Github

```sh
pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git
```
(you may need to run `pip` with root permission: `sudo pip install git+https://github.com/GIT_USER_ID/GIT_REPO_ID.git`)

Then import the package:
```python
import cloudmersive_documentai_api_client 
```

### Setuptools

Install via [Setuptools](http://pypi.python.org/pypi/setuptools).

```sh
python setup.py install --user
```
(or `sudo python setup.py install` to install the package for all users)

Then import the package:
```python
import cloudmersive_documentai_api_client
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## Documentation for API Endpoints

All URIs are relative to *https://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AnalyzeApi* | [**apply_rules**](docs/AnalyzeApi.md#apply_rules) | **POST** /document-ai/document/analyze/enforce-policy | Enforce Policies to a Document to allow or block it using Advanced AI
*ExtractApi* | [**extract_all_fields_and_tables**](docs/ExtractApi.md#extract_all_fields_and_tables) | **POST** /document-ai/document/extract/all | Extract All Fields and Tables of Data from a Document using AI
*ExtractApi* | [**extract_barcodes**](docs/ExtractApi.md#extract_barcodes) | **POST** /document-ai/document/extract/barcodes | Extract Barcodes of from a Document using AI
*ExtractApi* | [**extract_classification**](docs/ExtractApi.md#extract_classification) | **POST** /document-ai/document/extract/classify | Extract Classification or Category from a Document using AI
*ExtractApi* | [**extract_classification_advanced**](docs/ExtractApi.md#extract_classification_advanced) | **POST** /document-ai/document/extract/classify/advanced | Extract Classification or Category from a Document using Advanced AI
*ExtractApi* | [**extract_fields**](docs/ExtractApi.md#extract_fields) | **POST** /document-ai/document/extract/fields | Extract Field Values from a Document using AI
*ExtractApi* | [**extract_fields_advanced**](docs/ExtractApi.md#extract_fields_advanced) | **POST** /document-ai/document/extract/fields/advanced | Extract Field Values from a Document using Advanced AI
*ExtractApi* | [**extract_summary**](docs/ExtractApi.md#extract_summary) | **POST** /document-ai/document/extract/summary | Extract Summary from a Document using AI
*ExtractApi* | [**extract_tables**](docs/ExtractApi.md#extract_tables) | **POST** /document-ai/document/extract/tables | Extract Tables of Data from a Document using AI
*ExtractApi* | [**extract_text**](docs/ExtractApi.md#extract_text) | **POST** /document-ai/document/extract/text | Extract Text from a Document using AI
*RunBatchJobApi* | [**extract_all_fields_and_tables_from_document_batch_job**](docs/RunBatchJobApi.md#extract_all_fields_and_tables_from_document_batch_job) | **POST** /document-ai/document/batch-job/extract/all | Extract All Fields and Tables of Data from a Document using AI as a Batch Job
*RunBatchJobApi* | [**extract_classification_from_document_batch_job**](docs/RunBatchJobApi.md#extract_classification_from_document_batch_job) | **POST** /document-ai/document/batch-job/extract/classify | Extract Classification or Category from a Document using AI as a Batch Job
*RunBatchJobApi* | [**extract_fields_from_document_advanced_batch_job**](docs/RunBatchJobApi.md#extract_fields_from_document_advanced_batch_job) | **POST** /document-ai/document/batch-job/extract/fields/advanced | Extract Field Values from a Document using Advanced AI as a Batch Job
*RunBatchJobApi* | [**extract_text_from_document_batch_job**](docs/RunBatchJobApi.md#extract_text_from_document_batch_job) | **POST** /document-ai/document/batch-job/extract/text | Extract Text from a Document using AI as a Batch Job
*RunBatchJobApi* | [**get_async_job_status**](docs/RunBatchJobApi.md#get_async_job_status) | **GET** /document-ai/document/batch-job/batch-job/status | Get the status and result of an Extract Document Batch Job


## Documentation For Models

 - [AdvancedExtractClassificationRequest](docs/AdvancedExtractClassificationRequest.md)
 - [AdvancedExtractFieldsRequest](docs/AdvancedExtractFieldsRequest.md)
 - [DocumentAdvancedClassificationResult](docs/DocumentAdvancedClassificationResult.md)
 - [DocumentCategories](docs/DocumentCategories.md)
 - [DocumentClassificationResult](docs/DocumentClassificationResult.md)
 - [DocumentPolicyRequest](docs/DocumentPolicyRequest.md)
 - [DocumentPolicyResult](docs/DocumentPolicyResult.md)
 - [ExtractBarcodesAiResponse](docs/ExtractBarcodesAiResponse.md)
 - [ExtractDocumentBatchJobResult](docs/ExtractDocumentBatchJobResult.md)
 - [ExtractDocumentJobStatusResult](docs/ExtractDocumentJobStatusResult.md)
 - [ExtractFieldsAdvancedResponse](docs/ExtractFieldsAdvancedResponse.md)
 - [ExtractFieldsAndTablesResponse](docs/ExtractFieldsAndTablesResponse.md)
 - [ExtractFieldsResponse](docs/ExtractFieldsResponse.md)
 - [ExtractTablesResponse](docs/ExtractTablesResponse.md)
 - [ExtractTextResponse](docs/ExtractTextResponse.md)
 - [ExtractedBarcodeItem](docs/ExtractedBarcodeItem.md)
 - [ExtractedTextPage](docs/ExtractedTextPage.md)
 - [FieldAdvancedValue](docs/FieldAdvancedValue.md)
 - [FieldToExtract](docs/FieldToExtract.md)
 - [FieldValue](docs/FieldValue.md)
 - [PolicyRule](docs/PolicyRule.md)
 - [PolicyRuleViolation](docs/PolicyRuleViolation.md)
 - [SummarizeDocumentResponse](docs/SummarizeDocumentResponse.md)
 - [TableResult](docs/TableResult.md)
 - [TableResultCell](docs/TableResultCell.md)
 - [TableResultRow](docs/TableResultRow.md)


## Documentation For Authorization


## Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header


## Author




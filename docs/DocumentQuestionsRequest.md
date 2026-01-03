# DocumentQuestionsRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input_file** | **str** | Input file as a byte array | [optional] 
**questions_yes_no** | [**list[DocumentQuestionBoolean]**](DocumentQuestionBoolean.md) | Optional: Yes or No boolean questions to answer about the document | [optional] 
**questions_multiple_choice** | [**list[DocumentQuestionMultipleChoice]**](DocumentQuestionMultipleChoice.md) | Optional: Multiple choice questions to answer about the document | [optional] 
**questions_free_response** | [**list[DocumentQuestionFreeResponse]**](DocumentQuestionFreeResponse.md) | Optional: Free response questions to answer about the document | [optional] 
**recognition_mode** | **str** | Optional; Recognition mode - Normal (default) provides the highest accuracy but slower speed, while Normal provides faster response but lower accuracy for low quality images | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



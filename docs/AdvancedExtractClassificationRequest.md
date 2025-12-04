# AdvancedExtractClassificationRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**input_file** | **str** | Input document file to perform the operation on as a byte array | [optional] 
**categories** | [**list[DocumentCategories]**](DocumentCategories.md) | Possible categories for the document | [optional] 
**preprocessing** | **str** | Optional: Set the level of image pre-processing to enhance accuracy.  Possible values are &#39;Auto&#39;, &#39;SmoothEdges&#39;, &#39;SmoothEdgesPlus&#39;, &#39;Compatability&#39; and &#39;None&#39;.  Default is Auto.  Set to SmoothEdges to smooth harsh edges in the input image to enhance recognition accuracy.  Set to SmoothEdgesPlus to smooth harsh edges to a higher degree.  Set to Compatability for maximum PDF feature compatability. | [optional] 
**result_cross_check** | **str** | Optional: Set the level of output accuracy cross-checking to perform on the input.  Possible values are &#39;None&#39;, &#39;Advanced&#39;, &#39;Ultra&#39; and &#39;Hyper&#39;.  Default is None.  Ultra and Hyper will produce the highest accuracy but at the cost of longer processing times. | [optional] 
**maximum_pages_processed** | **int** | Optional: Limit the number of pages processed | [optional] 
**rotate_image_degrees** | **float** | Optional: Rotate the input image before recognition by the specified number of degrees; valid values range from -360 to +360. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



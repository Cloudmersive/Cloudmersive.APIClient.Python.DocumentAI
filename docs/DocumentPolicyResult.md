# DocumentPolicyResult

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**clean_result** | **bool** | True if the document complies with all of the policies, and false if it does not | [optional] 
**risk_score** | **float** | Risk score between 0.0 and 1.0 where values above 0.5 are increasing levels of risk | [optional] 
**rule_violations** | [**list[PolicyRuleViolation]**](PolicyRuleViolation.md) | Policy violations | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)



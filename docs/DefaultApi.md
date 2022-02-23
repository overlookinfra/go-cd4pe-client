# \DefaultApi

All URIs are relative to *http://localhost/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateToken**](DefaultApi.md#CreateToken) | **Post** /auth/token | Create a token associated with the passed in credentials
[**EvaluatePermissions**](DefaultApi.md#EvaluatePermissions) | **Post** /permitted | Evaluate permissions for a user
[**GetControlRepos**](DefaultApi.md#GetControlRepos) | **Get** /workspaces/{workspaceId}/controlrepos | 
[**GetUserInfo**](DefaultApi.md#GetUserInfo) | **Get** /user | Get information about the user associated with this token
[**ListPeIntegrationsWithToken**](DefaultApi.md#ListPeIntegrationsWithToken) | **Get** /internal/workspaces/{workspaceId}/integrations/pe | List PE integrations for a workspace



## CreateToken

> string CreateToken(ctx, optional)

Create a token associated with the passed in credentials

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***CreateTokenOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a CreateTokenOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **createTokenRequest** | [**optional.Interface of CreateTokenRequest**](CreateTokenRequest.md)|  | 

### Return type

**string**

### Authorization

[default](../README.md#default)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## EvaluatePermissions

> Permitted EvaluatePermissions(ctx, workspaceId, optional)

Evaluate permissions for a user

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**workspaceId** | **string**|  | 
 **optional** | ***EvaluatePermissionsOpts** | optional parameters | nil if no parameters

### Optional Parameters

Optional parameters are passed through a pointer to a EvaluatePermissionsOpts struct


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **evaluatePermissionsRequest** | [**optional.Interface of EvaluatePermissionsRequest**](EvaluatePermissionsRequest.md)|  | 

### Return type

[**Permitted**](Permitted.md)

### Authorization

[default](../README.md#default)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetControlRepos

> ControlRepo GetControlRepos(ctx, workspaceId)



Returns a list of Control Repos

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**workspaceId** | **string**|  | 

### Return type

[**ControlRepo**](ControlRepo.md)

### Authorization

[default](../README.md#default)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## GetUserInfo

> CurrentUserDetails GetUserInfo(ctx, )

Get information about the user associated with this token

### Required Parameters

This endpoint does not need any parameter.

### Return type

[**CurrentUserDetails**](CurrentUserDetails.md)

### Authorization

[default](../README.md#default)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


## ListPeIntegrationsWithToken

> ListPeIntegrationsWithTokenResponse ListPeIntegrationsWithToken(ctx, workspaceId)

List PE integrations for a workspace

List PE integrations with tokens for a workspace. This is a internal only api.

### Required Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
**ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
**workspaceId** | **string**| Identifies a workspace | 

### Return type

[**ListPeIntegrationsWithTokenResponse**](ListPEIntegrationsWithTokenResponse.md)

### Authorization

[default](../README.md#default)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


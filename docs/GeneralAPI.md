# \GeneralAPI

All URIs are relative to *https://studio.persianapi.com/index.php*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetWebServiceCommon1**](GeneralAPI.md#GetWebServiceCommon1) | **Get** /web-service/common/gold-currency-coin | داده های عمومی - بازار داخلی



## GetWebServiceCommon1

> CommonLocalResponse GetWebServiceCommon1(ctx).Format(format).Limit(limit).Page(page).Execute()

داده های عمومی - بازار داخلی



### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/sajadsafary/tgju"
)

func main() {
	format := "format_example" // string | فرمت خروجی (optional) (default to "json")
	limit := int32(56) // int32 | تعداد موارد ارایه شده در صفحه (optional) (default to 30)
	page := int32(56) // int32 | شماره صفحه برای ارائه دیتا (optional) (default to 1)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.GeneralAPI.GetWebServiceCommon1(context.Background()).Format(format).Limit(limit).Page(page).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `GeneralAPI.GetWebServiceCommon1``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `GetWebServiceCommon1`: CommonLocalResponse
	fmt.Fprintf(os.Stdout, "Response from `GeneralAPI.GetWebServiceCommon1`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiGetWebServiceCommon1Request struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **format** | **string** | فرمت خروجی | [default to &quot;json&quot;]
 **limit** | **int32** | تعداد موارد ارایه شده در صفحه | [default to 30]
 **page** | **int32** | شماره صفحه برای ارائه دیتا | [default to 1]

### Return type

[**CommonLocalResponse**](CommonLocalResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)


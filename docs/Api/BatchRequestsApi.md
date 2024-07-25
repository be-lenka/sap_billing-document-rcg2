# BeLenka\SAP\BillingDocumentRCG2\BatchRequestsApi

All URIs are relative to https://:/sap/opu/odata/sap/API_BILLING_DOCUMENT_SRV, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**batchPost()**](BatchRequestsApi.md#batchPost) | **POST** /$batch | Send a group of requests |


## `batchPost()`

```php
batchPost(): string
```

Send a group of requests

Group multiple requests into a single request payload, see [Batch Requests](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=152).  *Please note that \"Try it out\" is not supported for this request.*

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BatchRequestsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->batchPost();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BatchRequestsApi->batchPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

**string**

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: `multipart/mixed;boundary=request-separator`
- **Accept**: `multipart/mixed`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

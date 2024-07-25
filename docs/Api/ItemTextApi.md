# BeLenka\SAP\BillingDocumentRCG2\ItemTextApi

All URIs are relative to https://:/sap/opu/odata/sap/API_BILLING_DOCUMENT_SRV, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToItemTextGet()**](ItemTextApi.md#aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToItemTextGet) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;)/to_ItemText | Reads the item texts of a specific billing document. |
| [**aBillingDocumentItemTextBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemLanguageLanguageLongTextIDLongTextIDGet()**](ItemTextApi.md#aBillingDocumentItemTextBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemLanguageLanguageLongTextIDLongTextIDGet) | **GET** /A_BillingDocumentItemText(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,Language&#x3D;&#39;{Language}&#39;,LongTextID&#x3D;&#39;{LongTextID}&#39;) | Reads item texts for a specific language and long text ID. |
| [**aBillingDocumentItemTextGet()**](ItemTextApi.md#aBillingDocumentItemTextGet) | **GET** /A_BillingDocumentItemText | Reads item texts of all billing documents. |


## `aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToItemTextGet()`

```php
aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToItemTextGet($billing_document, $billing_document_item, $top, $skip, $filter, $inlinecount, $orderby, $select): \BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper5
```

Reads the item texts of a specific billing document.

Reads texts and related fields from an item of a specific billing document, which the consumer specifies by passing the billing document number and item number. The related fields include the language and long text ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemTextApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$billing_document_item = 'billing_document_item_example'; // string | Billing Item
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)

try {
    $result = $apiInstance->aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToItemTextGet($billing_document, $billing_document_item, $top, $skip, $filter, $inlinecount, $orderby, $select);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemTextApi->aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToItemTextGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **billing_document_item** | **string**| Billing Item | |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper5**](../Model/Wrapper5.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentItemTextBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemLanguageLanguageLongTextIDLongTextIDGet()`

```php
aBillingDocumentItemTextBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemLanguageLanguageLongTextIDLongTextIDGet($billing_document, $billing_document_item, $language, $long_text_id, $select): \BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentItemTextType
```

Reads item texts for a specific language and long text ID.

Reads texts and related fields of a specific billing document item. Consumers must pass the key fields billing document number, item number, language, and long text ID. The related fields include the language and long text ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemTextApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$billing_document_item = 'billing_document_item_example'; // string | Billing Item
$language = 'language_example'; // string | Language Key
$long_text_id = 'long_text_id_example'; // string | Text ID
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)

try {
    $result = $apiInstance->aBillingDocumentItemTextBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemLanguageLanguageLongTextIDLongTextIDGet($billing_document, $billing_document_item, $language, $long_text_id, $select);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemTextApi->aBillingDocumentItemTextBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemLanguageLanguageLongTextIDLongTextIDGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **billing_document_item** | **string**| Billing Item | |
| **language** | **string**| Language Key | |
| **long_text_id** | **string**| Text ID | |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentItemTextType**](../Model/ABillingDocumentItemTextType.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentItemTextGet()`

```php
aBillingDocumentItemTextGet($top, $skip, $filter, $inlinecount, $orderby, $select): \BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper5
```

Reads item texts of all billing documents.

Reads texts and related fields from the items of all billing documents in the system. The related fields include the language and long text ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemTextApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)

try {
    $result = $apiInstance->aBillingDocumentItemTextGet($top, $skip, $filter, $inlinecount, $orderby, $select);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemTextApi->aBillingDocumentItemTextGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper5**](../Model/Wrapper5.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

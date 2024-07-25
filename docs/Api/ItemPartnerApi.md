# BeLenka\SAP\BillingDocumentRCG2\ItemPartnerApi

All URIs are relative to https://:/sap/opu/odata/sap/API_BILLING_DOCUMENT_SRV, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPartnerGet()**](ItemPartnerApi.md#aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPartnerGet) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;)/to_Partner | Reads the item business partners of a specific billing document item. |
| [**aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionGet()**](ItemPartnerApi.md#aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionGet) | **GET** /A_BillingDocumentItemPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;) | Reads item business partners of an item and with a specific partner function in a specific billing document. |
| [**aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentGet()**](ItemPartnerApi.md#aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentGet) | **GET** /A_BillingDocumentItemPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;)/to_BillingDocument | Reads the billing document header for a specific item partner function. |
| [**aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentItemGet()**](ItemPartnerApi.md#aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentItemGet) | **GET** /A_BillingDocumentItemPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;)/to_BillingDocumentItem | Reads a billing document item for a specific item partner function. |
| [**aBillingDocumentItemPartnerGet()**](ItemPartnerApi.md#aBillingDocumentItemPartnerGet) | **GET** /A_BillingDocumentItemPartner | Reads item business partners for all billing documents. |


## `aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPartnerGet()`

```php
aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPartnerGet($billing_document, $billing_document_item, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper6
```

Reads the item business partners of a specific billing document item.

Reads business partner data from a specific item of a specific billing document. The consumer must specify the billing document number and item number. Includes fields such as partner function, customer, contact person, and more.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemPartnerApi(
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
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPartnerGet($billing_document, $billing_document_item, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemPartnerApi->aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPartnerGet: ', $e->getMessage(), PHP_EOL;
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
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper6**](../Model/Wrapper6.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionGet()`

```php
aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionGet($billing_document, $billing_document_item, $partner_function, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentItemPartnerType
```

Reads item business partners of an item and with a specific partner function in a specific billing document.

Reads item-level business partners with a specific partner function of a specific billing document. Consumers must specify the billing document number, billing document item, and partner function.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemPartnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$billing_document_item = 'billing_document_item_example'; // string | Billing Item
$partner_function = 'partner_function_example'; // string | Partner Function
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionGet($billing_document, $billing_document_item, $partner_function, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemPartnerApi->aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **billing_document_item** | **string**| Billing Item | |
| **partner_function** | **string**| Partner Function | |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentItemPartnerType**](../Model/ABillingDocumentItemPartnerType.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentGet()`

```php
aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentGet($billing_document, $billing_document_item, $partner_function, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentType
```

Reads the billing document header for a specific item partner function.

Reads the billing document header fields for a specific item-level partner function. Includes fields such as the document number, billing date, total amount, billing type, and more. Consumers must pass the following key fields: billing document number, item number, and item partner function.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemPartnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$billing_document_item = 'billing_document_item_example'; // string | Billing Item
$partner_function = 'partner_function_example'; // string | Partner Function
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentGet($billing_document, $billing_document_item, $partner_function, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemPartnerApi->aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **billing_document_item** | **string**| Billing Item | |
| **partner_function** | **string**| Partner Function | |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentType**](../Model/ABillingDocumentType.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentItemGet()`

```php
aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentItemGet($billing_document, $billing_document_item, $partner_function, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentItemType
```

Reads a billing document item for a specific item partner function.

Reads billing document item fields for a specific item-level partner function. Includes fields such as the item number, billing quantity, product, net amount, and more. Consumers must pass the following key fields: billing document number, item number, and item partner function.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemPartnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$billing_document_item = 'billing_document_item_example'; // string | Billing Item
$partner_function = 'partner_function_example'; // string | Partner Function
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentItemGet($billing_document, $billing_document_item, $partner_function, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemPartnerApi->aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentItemGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **billing_document_item** | **string**| Billing Item | |
| **partner_function** | **string**| Partner Function | |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentItemType**](../Model/ABillingDocumentItemType.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentItemPartnerGet()`

```php
aBillingDocumentItemPartnerGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper6
```

Reads item business partners for all billing documents.

Reads business partner data from the items of all billing documents in the system. This includes fields such as partner function, customer, contact person, and more.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemPartnerApi(
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
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentItemPartnerGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemPartnerApi->aBillingDocumentItemPartnerGet: ', $e->getMessage(), PHP_EOL;
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
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper6**](../Model/Wrapper6.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

# BeLenka\SAP\BillingDocumentRCG2\ItemPricingElementApi

All URIs are relative to https://:/sap/opu/odata/sap/API_BILLING_DOCUMENT_SRV, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPricingElementGet()**](ItemPricingElementApi.md#aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPricingElementGet) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;)/to_PricingElement | Reads the item pricing elements of a specific billing document item. |
| [**aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterGet()**](ItemPricingElementApi.md#aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterGet) | **GET** /A_BillingDocumentItemPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;) | Reads the item pricing elements for a specific item and item pricing element. |
| [**aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet()**](ItemPricingElementApi.md#aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet) | **GET** /A_BillingDocumentItemPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;)/to_BillingDocument | Reads the billing document header for a specific item and pricing element. |
| [**aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentItemGet()**](ItemPricingElementApi.md#aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentItemGet) | **GET** /A_BillingDocumentItemPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;)/to_BillingDocumentItem | Reads a billing document item for a specific item and item-level pricing element. |
| [**aBillingDocumentItemPrcgElmntGet()**](ItemPricingElementApi.md#aBillingDocumentItemPrcgElmntGet) | **GET** /A_BillingDocumentItemPrcgElmnt | Reads item pricing elements of all billing documents. |


## `aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPricingElementGet()`

```php
aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPricingElementGet($billing_document, $billing_document_item, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper7
```

Reads the item pricing elements of a specific billing document item.

Reads pricing element data from a specific item of a specific billing document. The consumer must specify the billing document number and item number. Includes fields such as condition type, condition currency, condition quantity, and more.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemPricingElementApi(
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
    $result = $apiInstance->aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPricingElementGet($billing_document, $billing_document_item, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemPricingElementApi->aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPricingElementGet: ', $e->getMessage(), PHP_EOL;
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

[**\BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper7**](../Model/Wrapper7.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterGet()`

```php
aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterGet($billing_document, $billing_document_item, $pricing_procedure_step, $pricing_procedure_counter, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentItemPrcgElmntType
```

Reads the item pricing elements for a specific item and item pricing element.

Reads pricing element data from a specific item and for a specific item pricing element. Includes fields such as condition type, condition currency, condition quantity, and more. Consumers must pass the following key fields: billing document number, item number pricing procedure step, and pricing procedure counter.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemPricingElementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$billing_document_item = 'billing_document_item_example'; // string | Billing Item
$pricing_procedure_step = 'pricing_procedure_step_example'; // string | Step Number
$pricing_procedure_counter = 'pricing_procedure_counter_example'; // string | Condition Counter
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterGet($billing_document, $billing_document_item, $pricing_procedure_step, $pricing_procedure_counter, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemPricingElementApi->aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **billing_document_item** | **string**| Billing Item | |
| **pricing_procedure_step** | **string**| Step Number | |
| **pricing_procedure_counter** | **string**| Condition Counter | |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentItemPrcgElmntType**](../Model/ABillingDocumentItemPrcgElmntType.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet()`

```php
aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet($billing_document, $billing_document_item, $pricing_procedure_step, $pricing_procedure_counter, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentType
```

Reads the billing document header for a specific item and pricing element.

Reads the billing document header fields for a specific item and pricing element. Includes fields such as the document number, billing date, total amount, billing type, and more. Consumers must pass the following key fields: billing document number, item number, pricing procedure step, and pricing procedure counter.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemPricingElementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$billing_document_item = 'billing_document_item_example'; // string | Billing Item
$pricing_procedure_step = 'pricing_procedure_step_example'; // string | Step Number
$pricing_procedure_counter = 'pricing_procedure_counter_example'; // string | Condition Counter
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet($billing_document, $billing_document_item, $pricing_procedure_step, $pricing_procedure_counter, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemPricingElementApi->aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **billing_document_item** | **string**| Billing Item | |
| **pricing_procedure_step** | **string**| Step Number | |
| **pricing_procedure_counter** | **string**| Condition Counter | |
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

## `aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentItemGet()`

```php
aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentItemGet($billing_document, $billing_document_item, $pricing_procedure_step, $pricing_procedure_counter, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentItemType
```

Reads a billing document item for a specific item and item-level pricing element.

Reads billing document item fields for a specific item and item-level pricing element. Includes fields such as the item number, billing quantity, product, net amount, and more. Consumers must pass the following key fields: billing document number, item number, pricing procedure step, and pricing procedure counter.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemPricingElementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$billing_document_item = 'billing_document_item_example'; // string | Billing Item
$pricing_procedure_step = 'pricing_procedure_step_example'; // string | Step Number
$pricing_procedure_counter = 'pricing_procedure_counter_example'; // string | Condition Counter
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentItemGet($billing_document, $billing_document_item, $pricing_procedure_step, $pricing_procedure_counter, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemPricingElementApi->aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentItemGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **billing_document_item** | **string**| Billing Item | |
| **pricing_procedure_step** | **string**| Step Number | |
| **pricing_procedure_counter** | **string**| Condition Counter | |
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

## `aBillingDocumentItemPrcgElmntGet()`

```php
aBillingDocumentItemPrcgElmntGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper7
```

Reads item pricing elements of all billing documents.

Reads pricing element data from the items of all billing documents in the system. Includes fields such as condition type, condition currency, condition quantity, and more.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\ItemPricingElementApi(
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
    $result = $apiInstance->aBillingDocumentItemPrcgElmntGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ItemPricingElementApi->aBillingDocumentItemPrcgElmntGet: ', $e->getMessage(), PHP_EOL;
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

[**\BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper7**](../Model/Wrapper7.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

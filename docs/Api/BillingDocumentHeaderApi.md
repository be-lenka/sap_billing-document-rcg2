# BeLenka\SAP\BillingDocumentRCG2\BillingDocumentHeaderApi

All URIs are relative to https://:/sap/opu/odata/sap/API_BILLING_DOCUMENT_SRV, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**aBillingDocumentBillingDocumentGet()**](BillingDocumentHeaderApi.md#aBillingDocumentBillingDocumentGet) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;) | Reads the header of a specific billing document. |
| [**aBillingDocumentBillingDocumentToItemGet()**](BillingDocumentHeaderApi.md#aBillingDocumentBillingDocumentToItemGet) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;)/to_Item | Reads all items of a specific billing document. |
| [**aBillingDocumentBillingDocumentToPartnerGet()**](BillingDocumentHeaderApi.md#aBillingDocumentBillingDocumentToPartnerGet) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;)/to_Partner | Reads the header business partners of a specific billing document. |
| [**aBillingDocumentBillingDocumentToPricingElementGet()**](BillingDocumentHeaderApi.md#aBillingDocumentBillingDocumentToPricingElementGet) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;)/to_PricingElement | Reads the header pricing elements of a specific billing document. |
| [**aBillingDocumentBillingDocumentToTextGet()**](BillingDocumentHeaderApi.md#aBillingDocumentBillingDocumentToTextGet) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;)/to_Text | Reads the header texts of a specific billing document. |
| [**aBillingDocumentGet()**](BillingDocumentHeaderApi.md#aBillingDocumentGet) | **GET** /A_BillingDocument | Reads all billing document headers. |
| [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToBillingDocumentGet()**](BillingDocumentHeaderApi.md#aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToBillingDocumentGet) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;)/to_BillingDocument | Reads the billing document header for a specific item. |
| [**aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentGet()**](BillingDocumentHeaderApi.md#aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentGet) | **GET** /A_BillingDocumentItemPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;)/to_BillingDocument | Reads the billing document header for a specific item partner function. |
| [**aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet()**](BillingDocumentHeaderApi.md#aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet) | **GET** /A_BillingDocumentItemPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;)/to_BillingDocument | Reads the billing document header for a specific item and pricing element. |
| [**aBillingDocumentPartnerBillingDocumentBillingDocumentPartnerFunctionPartnerFunctionToBillingDocumentGet()**](BillingDocumentHeaderApi.md#aBillingDocumentPartnerBillingDocumentBillingDocumentPartnerFunctionPartnerFunctionToBillingDocumentGet) | **GET** /A_BillingDocumentPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;)/to_BillingDocument | Reads the billing document header for a specific header partner function. |
| [**aBillingDocumentPrcgElmntBillingDocumentBillingDocumentPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet()**](BillingDocumentHeaderApi.md#aBillingDocumentPrcgElmntBillingDocumentBillingDocumentPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet) | **GET** /A_BillingDocumentPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;)/to_BillingDocument | Reads the billing document header for a specific header pricing element. |
| [**cancelPost()**](BillingDocumentHeaderApi.md#cancelPost) | **POST** /Cancel | Cancels one specific billing document. |
| [**getPDFGet()**](BillingDocumentHeaderApi.md#getPDFGet) | **GET** /GetPDF | Retrieves a specific billing document in PDF format. |


## `aBillingDocumentBillingDocumentGet()`

```php
aBillingDocumentBillingDocumentGet($billing_document, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentType
```

Reads the header of a specific billing document.

Reads the header fields of a specific billing document, which the consumer specifies by passing the billing document number. Includes fields such as the document number, billing date, total amount, billing type, and more.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentBillingDocumentGet($billing_document, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingDocumentHeaderApi->aBillingDocumentBillingDocumentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
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

## `aBillingDocumentBillingDocumentToItemGet()`

```php
aBillingDocumentBillingDocumentToItemGet($billing_document, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper1
```

Reads all items of a specific billing document.

Reads all item fields of a specific billing document, which the consumer specifies by passing the billing document number. Includes fields such as the item number, billing quantity, product, net amount, and more.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentBillingDocumentToItemGet($billing_document, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingDocumentHeaderApi->aBillingDocumentBillingDocumentToItemGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper1**](../Model/Wrapper1.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentBillingDocumentToPartnerGet()`

```php
aBillingDocumentBillingDocumentToPartnerGet($billing_document, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper2
```

Reads the header business partners of a specific billing document.

Reads the business partner data from the header of a specific billing document, which the consumer specifies by passing the billing document number. Includes fields such as partner function, customer, contact person, and more.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentBillingDocumentToPartnerGet($billing_document, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingDocumentHeaderApi->aBillingDocumentBillingDocumentToPartnerGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper2**](../Model/Wrapper2.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentBillingDocumentToPricingElementGet()`

```php
aBillingDocumentBillingDocumentToPricingElementGet($billing_document, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper3
```

Reads the header pricing elements of a specific billing document.

Reads the pricing element data from the header of a specific billing document, which the consumer specifies by passing the billing document number. This includes fields such as condition type, condition currency, condition quantity, and more.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentBillingDocumentToPricingElementGet($billing_document, $top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingDocumentHeaderApi->aBillingDocumentBillingDocumentToPricingElementGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |
| **expand** | [**string[]**](../Model/string.md)| Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;63) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper3**](../Model/Wrapper3.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentBillingDocumentToTextGet()`

```php
aBillingDocumentBillingDocumentToTextGet($billing_document, $top, $skip, $filter, $inlinecount, $orderby, $select): \BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper4
```

Reads the header texts of a specific billing document.

Reads texts and related fields from the header of a specific billing document, which the consumer specifies by passing the billing document number. Texts typically provide billing instructions or notes for customers. The related fields include the language and long text ID.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$top = 50; // int | Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=66)
$skip = 56; // int | Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$filter = 'filter_example'; // string | Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=64)
$inlinecount = 'inlinecount_example'; // string | Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=67)
$orderby = array('orderby_example'); // string[] | Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=65)
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)

try {
    $result = $apiInstance->aBillingDocumentBillingDocumentToTextGet($billing_document, $top, $skip, $filter, $inlinecount, $orderby, $select);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingDocumentHeaderApi->aBillingDocumentBillingDocumentToTextGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **top** | **int**| Show only the first n items, see [Paging - Top](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;66) | [optional] |
| **skip** | **int**| Skip the first n items, see [Paging - Skip](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **filter** | **string**| Filter items by property values, see [Filtering](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;64) | [optional] |
| **inlinecount** | **string**| Include count of items, see [Inlinecount](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;67) | [optional] |
| **orderby** | [**string[]**](../Model/string.md)| Order items by property values, see [Sorting](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;65) | [optional] |
| **select** | [**string[]**](../Model/string.md)| Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page&#x3D;68) | [optional] |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper4**](../Model/Wrapper4.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentGet()`

```php
aBillingDocumentGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper
```

Reads all billing document headers.

Reads the header fields of all billing documents in the system. Includes fields such as the document number, billing date, total amount, billing type, and more.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
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
    $result = $apiInstance->aBillingDocumentGet($top, $skip, $filter, $inlinecount, $orderby, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingDocumentHeaderApi->aBillingDocumentGet: ', $e->getMessage(), PHP_EOL;
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

[**\BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper**](../Model/Wrapper.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToBillingDocumentGet()`

```php
aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToBillingDocumentGet($billing_document, $billing_document_item, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentType
```

Reads the billing document header for a specific item.

Reads the billing document header fields for a specific item. Includes fields such as the document number, billing date, total amount, billing type, and more. Consumers must pass the following key fields: billing document number, item number.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$billing_document_item = 'billing_document_item_example'; // string | Billing Item
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToBillingDocumentGet($billing_document, $billing_document_item, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingDocumentHeaderApi->aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToBillingDocumentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
| **billing_document_item** | **string**| Billing Item | |
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


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
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
    echo 'Exception when calling BillingDocumentHeaderApi->aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentGet: ', $e->getMessage(), PHP_EOL;
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


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
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
    echo 'Exception when calling BillingDocumentHeaderApi->aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet: ', $e->getMessage(), PHP_EOL;
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

## `aBillingDocumentPartnerBillingDocumentBillingDocumentPartnerFunctionPartnerFunctionToBillingDocumentGet()`

```php
aBillingDocumentPartnerBillingDocumentBillingDocumentPartnerFunctionPartnerFunctionToBillingDocumentGet($billing_document, $partner_function, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentType
```

Reads the billing document header for a specific header partner function.

Reads the billing document header fields for a specific header-level partner function. Includes fields such as the document number, billing date, total amount, billing type, and more. Consumers must pass the following key fields: billing document number and partner function.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$partner_function = 'partner_function_example'; // string | Partner Function
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentPartnerBillingDocumentBillingDocumentPartnerFunctionPartnerFunctionToBillingDocumentGet($billing_document, $partner_function, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingDocumentHeaderApi->aBillingDocumentPartnerBillingDocumentBillingDocumentPartnerFunctionPartnerFunctionToBillingDocumentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
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

## `aBillingDocumentPrcgElmntBillingDocumentBillingDocumentPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet()`

```php
aBillingDocumentPrcgElmntBillingDocumentBillingDocumentPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet($billing_document, $pricing_procedure_step, $pricing_procedure_counter, $select, $expand): \BeLenka\SAP\BillingDocumentRCG2\Model\ABillingDocumentType
```

Reads the billing document header for a specific header pricing element.

Reads the billing document header fields for a specific header-level pricing element. Includes fields such as the document number, billing date, total amount, billing type, and more. Consumers must pass the following key fields: billing document number, pricing procedure step, and pricing procedure counter.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Billing Document
$pricing_procedure_step = 'pricing_procedure_step_example'; // string | Step Number
$pricing_procedure_counter = 'pricing_procedure_counter_example'; // string | Condition Counter
$select = array('select_example'); // string[] | Select properties to be returned, see [Select](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=68)
$expand = array('expand_example'); // string[] | Expand related entities, see [Expand](https://help.sap.com/doc/5890d27be418427993fafa6722cdc03b/Cloud/en-US/OdataV2.pdf#page=63)

try {
    $result = $apiInstance->aBillingDocumentPrcgElmntBillingDocumentBillingDocumentPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet($billing_document, $pricing_procedure_step, $pricing_procedure_counter, $select, $expand);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingDocumentHeaderApi->aBillingDocumentPrcgElmntBillingDocumentBillingDocumentPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Billing Document | |
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

## `cancelPost()`

```php
cancelPost($billing_document): \BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper8
```

Cancels one specific billing document.

Cancels one specific billing document in the system, which the consumer specifies by passing the billing document number. To cancel multiple billing documents simultaneously, use a batch request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Value needs to be enclosed in single quotes

try {
    $result = $apiInstance->cancelPost($billing_document);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingDocumentHeaderApi->cancelPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Value needs to be enclosed in single quotes | |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\Wrapper8**](../Model/Wrapper8.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPDFGet()`

```php
getPDFGet($billing_document): \BeLenka\SAP\BillingDocumentRCG2\Model\GetPDFResult
```

Retrieves a specific billing document in PDF format.

Retrieves a specific billing document from the system in PDF format, which shows how the billing document looks after it has been output to PDF. Consumer must specify the billing document number.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: BasicAuth
$config = BeLenka\SAP\BillingDocumentRCG2\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new BeLenka\SAP\BillingDocumentRCG2\Api\BillingDocumentHeaderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$billing_document = 'billing_document_example'; // string | Value needs to be enclosed in single quotes

try {
    $result = $apiInstance->getPDFGet($billing_document);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BillingDocumentHeaderApi->getPDFGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **billing_document** | **string**| Value needs to be enclosed in single quotes | |

### Return type

[**\BeLenka\SAP\BillingDocumentRCG2\Model\GetPDFResult**](../Model/GetPDFResult.md)

### Authorization

[BasicAuth](../../README.md#BasicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

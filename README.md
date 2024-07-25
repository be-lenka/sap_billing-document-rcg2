# OpenAPIClient-php

Consumers of this inbound service can read and cancel billing documents inside your system by sending OData requests. In addition, they can request entire billing documents in PDF format. The service makes billing document data available through its header, item, business partner, and pricing element entities.


## Installation & Usage

### Requirements

PHP 7.4 and later.
Should also work with PHP 8.0.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## API Endpoints

All URIs are relative to *https://:/sap/opu/odata/sap/API_BILLING_DOCUMENT_SRV*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BatchRequestsApi* | [**batchPost**](docs/Api/BatchRequestsApi.md#batchpost) | **POST** /$batch | Send a group of requests
*BillingDocumentHeaderApi* | [**aBillingDocumentBillingDocumentGet**](docs/Api/BillingDocumentHeaderApi.md#abillingdocumentbillingdocumentget) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;) | Reads the header of a specific billing document.
*BillingDocumentHeaderApi* | [**aBillingDocumentBillingDocumentToItemGet**](docs/Api/BillingDocumentHeaderApi.md#abillingdocumentbillingdocumenttoitemget) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;)/to_Item | Reads all items of a specific billing document.
*BillingDocumentHeaderApi* | [**aBillingDocumentBillingDocumentToPartnerGet**](docs/Api/BillingDocumentHeaderApi.md#abillingdocumentbillingdocumenttopartnerget) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;)/to_Partner | Reads the header business partners of a specific billing document.
*BillingDocumentHeaderApi* | [**aBillingDocumentBillingDocumentToPricingElementGet**](docs/Api/BillingDocumentHeaderApi.md#abillingdocumentbillingdocumenttopricingelementget) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;)/to_PricingElement | Reads the header pricing elements of a specific billing document.
*BillingDocumentHeaderApi* | [**aBillingDocumentBillingDocumentToTextGet**](docs/Api/BillingDocumentHeaderApi.md#abillingdocumentbillingdocumenttotextget) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;)/to_Text | Reads the header texts of a specific billing document.
*BillingDocumentHeaderApi* | [**aBillingDocumentGet**](docs/Api/BillingDocumentHeaderApi.md#abillingdocumentget) | **GET** /A_BillingDocument | Reads all billing document headers.
*BillingDocumentHeaderApi* | [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToBillingDocumentGet**](docs/Api/BillingDocumentHeaderApi.md#abillingdocumentitembillingdocumentbillingdocumentbillingdocumentitembillingdocumentitemtobillingdocumentget) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;)/to_BillingDocument | Reads the billing document header for a specific item.
*BillingDocumentHeaderApi* | [**aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentGet**](docs/Api/BillingDocumentHeaderApi.md#abillingdocumentitempartnerbillingdocumentbillingdocumentbillingdocumentitembillingdocumentitempartnerfunctionpartnerfunctiontobillingdocumentget) | **GET** /A_BillingDocumentItemPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;)/to_BillingDocument | Reads the billing document header for a specific item partner function.
*BillingDocumentHeaderApi* | [**aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet**](docs/Api/BillingDocumentHeaderApi.md#abillingdocumentitemprcgelmntbillingdocumentbillingdocumentbillingdocumentitembillingdocumentitempricingproceduresteppricingproceduresteppricingprocedurecounterpricingprocedurecountertobillingdocumentget) | **GET** /A_BillingDocumentItemPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;)/to_BillingDocument | Reads the billing document header for a specific item and pricing element.
*BillingDocumentHeaderApi* | [**aBillingDocumentPartnerBillingDocumentBillingDocumentPartnerFunctionPartnerFunctionToBillingDocumentGet**](docs/Api/BillingDocumentHeaderApi.md#abillingdocumentpartnerbillingdocumentbillingdocumentpartnerfunctionpartnerfunctiontobillingdocumentget) | **GET** /A_BillingDocumentPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;)/to_BillingDocument | Reads the billing document header for a specific header partner function.
*BillingDocumentHeaderApi* | [**aBillingDocumentPrcgElmntBillingDocumentBillingDocumentPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet**](docs/Api/BillingDocumentHeaderApi.md#abillingdocumentprcgelmntbillingdocumentbillingdocumentpricingproceduresteppricingproceduresteppricingprocedurecounterpricingprocedurecountertobillingdocumentget) | **GET** /A_BillingDocumentPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;)/to_BillingDocument | Reads the billing document header for a specific header pricing element.
*BillingDocumentHeaderApi* | [**cancelPost**](docs/Api/BillingDocumentHeaderApi.md#cancelpost) | **POST** /Cancel | Cancels one specific billing document.
*BillingDocumentHeaderApi* | [**getPDFGet**](docs/Api/BillingDocumentHeaderApi.md#getpdfget) | **GET** /GetPDF | Retrieves a specific billing document in PDF format.
*BillingDocumentItemApi* | [**aBillingDocumentBillingDocumentToItemGet**](docs/Api/BillingDocumentItemApi.md#abillingdocumentbillingdocumenttoitemget) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;)/to_Item | Reads all items of a specific billing document.
*BillingDocumentItemApi* | [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemGet**](docs/Api/BillingDocumentItemApi.md#abillingdocumentitembillingdocumentbillingdocumentbillingdocumentitembillingdocumentitemget) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;) | Reads a specific billing document item.
*BillingDocumentItemApi* | [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToBillingDocumentGet**](docs/Api/BillingDocumentItemApi.md#abillingdocumentitembillingdocumentbillingdocumentbillingdocumentitembillingdocumentitemtobillingdocumentget) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;)/to_BillingDocument | Reads the billing document header for a specific item.
*BillingDocumentItemApi* | [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToItemTextGet**](docs/Api/BillingDocumentItemApi.md#abillingdocumentitembillingdocumentbillingdocumentbillingdocumentitembillingdocumentitemtoitemtextget) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;)/to_ItemText | Reads the item texts of a specific billing document.
*BillingDocumentItemApi* | [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPartnerGet**](docs/Api/BillingDocumentItemApi.md#abillingdocumentitembillingdocumentbillingdocumentbillingdocumentitembillingdocumentitemtopartnerget) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;)/to_Partner | Reads the item business partners of a specific billing document item.
*BillingDocumentItemApi* | [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPricingElementGet**](docs/Api/BillingDocumentItemApi.md#abillingdocumentitembillingdocumentbillingdocumentbillingdocumentitembillingdocumentitemtopricingelementget) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;)/to_PricingElement | Reads the item pricing elements of a specific billing document item.
*BillingDocumentItemApi* | [**aBillingDocumentItemGet**](docs/Api/BillingDocumentItemApi.md#abillingdocumentitemget) | **GET** /A_BillingDocumentItem | Reads all billing document Items.
*BillingDocumentItemApi* | [**aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentItemGet**](docs/Api/BillingDocumentItemApi.md#abillingdocumentitempartnerbillingdocumentbillingdocumentbillingdocumentitembillingdocumentitempartnerfunctionpartnerfunctiontobillingdocumentitemget) | **GET** /A_BillingDocumentItemPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;)/to_BillingDocumentItem | Reads a billing document item for a specific item partner function.
*BillingDocumentItemApi* | [**aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentItemGet**](docs/Api/BillingDocumentItemApi.md#abillingdocumentitemprcgelmntbillingdocumentbillingdocumentbillingdocumentitembillingdocumentitempricingproceduresteppricingproceduresteppricingprocedurecounterpricingprocedurecountertobillingdocumentitemget) | **GET** /A_BillingDocumentItemPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;)/to_BillingDocumentItem | Reads a billing document item for a specific item and item-level pricing element.
*HeaderPartnerApi* | [**aBillingDocumentBillingDocumentToPartnerGet**](docs/Api/HeaderPartnerApi.md#abillingdocumentbillingdocumenttopartnerget) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;)/to_Partner | Reads the header business partners of a specific billing document.
*HeaderPartnerApi* | [**aBillingDocumentPartnerBillingDocumentBillingDocumentPartnerFunctionPartnerFunctionGet**](docs/Api/HeaderPartnerApi.md#abillingdocumentpartnerbillingdocumentbillingdocumentpartnerfunctionpartnerfunctionget) | **GET** /A_BillingDocumentPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;) | Reads the header business partners of a specific billing document and with a specific partner function.
*HeaderPartnerApi* | [**aBillingDocumentPartnerBillingDocumentBillingDocumentPartnerFunctionPartnerFunctionToBillingDocumentGet**](docs/Api/HeaderPartnerApi.md#abillingdocumentpartnerbillingdocumentbillingdocumentpartnerfunctionpartnerfunctiontobillingdocumentget) | **GET** /A_BillingDocumentPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;)/to_BillingDocument | Reads the billing document header for a specific header partner function.
*HeaderPartnerApi* | [**aBillingDocumentPartnerGet**](docs/Api/HeaderPartnerApi.md#abillingdocumentpartnerget) | **GET** /A_BillingDocumentPartner | Reads the header business partners of all billing documents.
*HeaderPricingElementApi* | [**aBillingDocumentBillingDocumentToPricingElementGet**](docs/Api/HeaderPricingElementApi.md#abillingdocumentbillingdocumenttopricingelementget) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;)/to_PricingElement | Reads the header pricing elements of a specific billing document.
*HeaderPricingElementApi* | [**aBillingDocumentPrcgElmntBillingDocumentBillingDocumentPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterGet**](docs/Api/HeaderPricingElementApi.md#abillingdocumentprcgelmntbillingdocumentbillingdocumentpricingproceduresteppricingproceduresteppricingprocedurecounterpricingprocedurecounterget) | **GET** /A_BillingDocumentPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;) | Reads the header pricing elements of a specific billing document and specific pricing element.
*HeaderPricingElementApi* | [**aBillingDocumentPrcgElmntBillingDocumentBillingDocumentPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet**](docs/Api/HeaderPricingElementApi.md#abillingdocumentprcgelmntbillingdocumentbillingdocumentpricingproceduresteppricingproceduresteppricingprocedurecounterpricingprocedurecountertobillingdocumentget) | **GET** /A_BillingDocumentPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;)/to_BillingDocument | Reads the billing document header for a specific header pricing element.
*HeaderPricingElementApi* | [**aBillingDocumentPrcgElmntGet**](docs/Api/HeaderPricingElementApi.md#abillingdocumentprcgelmntget) | **GET** /A_BillingDocumentPrcgElmnt | Reads header pricing elements of all billing documents.
*HeaderTextApi* | [**aBillingDocumentBillingDocumentToTextGet**](docs/Api/HeaderTextApi.md#abillingdocumentbillingdocumenttotextget) | **GET** /A_BillingDocument(&#39;{BillingDocument}&#39;)/to_Text | Reads the header texts of a specific billing document.
*HeaderTextApi* | [**aBillingDocumentTextBillingDocumentBillingDocumentLanguageLanguageLongTextIDLongTextIDGet**](docs/Api/HeaderTextApi.md#abillingdocumenttextbillingdocumentbillingdocumentlanguagelanguagelongtextidlongtextidget) | **GET** /A_BillingDocumentText(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,Language&#x3D;&#39;{Language}&#39;,LongTextID&#x3D;&#39;{LongTextID}&#39;) | Reads the header texts of a specific billing document for a specific language and long text ID.
*HeaderTextApi* | [**aBillingDocumentTextGet**](docs/Api/HeaderTextApi.md#abillingdocumenttextget) | **GET** /A_BillingDocumentText | Reads the header texts of all billing documents.
*ItemPartnerApi* | [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPartnerGet**](docs/Api/ItemPartnerApi.md#abillingdocumentitembillingdocumentbillingdocumentbillingdocumentitembillingdocumentitemtopartnerget) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;)/to_Partner | Reads the item business partners of a specific billing document item.
*ItemPartnerApi* | [**aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionGet**](docs/Api/ItemPartnerApi.md#abillingdocumentitempartnerbillingdocumentbillingdocumentbillingdocumentitembillingdocumentitempartnerfunctionpartnerfunctionget) | **GET** /A_BillingDocumentItemPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;) | Reads item business partners of an item and with a specific partner function in a specific billing document.
*ItemPartnerApi* | [**aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentGet**](docs/Api/ItemPartnerApi.md#abillingdocumentitempartnerbillingdocumentbillingdocumentbillingdocumentitembillingdocumentitempartnerfunctionpartnerfunctiontobillingdocumentget) | **GET** /A_BillingDocumentItemPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;)/to_BillingDocument | Reads the billing document header for a specific item partner function.
*ItemPartnerApi* | [**aBillingDocumentItemPartnerBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPartnerFunctionPartnerFunctionToBillingDocumentItemGet**](docs/Api/ItemPartnerApi.md#abillingdocumentitempartnerbillingdocumentbillingdocumentbillingdocumentitembillingdocumentitempartnerfunctionpartnerfunctiontobillingdocumentitemget) | **GET** /A_BillingDocumentItemPartner(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PartnerFunction&#x3D;&#39;{PartnerFunction}&#39;)/to_BillingDocumentItem | Reads a billing document item for a specific item partner function.
*ItemPartnerApi* | [**aBillingDocumentItemPartnerGet**](docs/Api/ItemPartnerApi.md#abillingdocumentitempartnerget) | **GET** /A_BillingDocumentItemPartner | Reads item business partners for all billing documents.
*ItemPricingElementApi* | [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToPricingElementGet**](docs/Api/ItemPricingElementApi.md#abillingdocumentitembillingdocumentbillingdocumentbillingdocumentitembillingdocumentitemtopricingelementget) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;)/to_PricingElement | Reads the item pricing elements of a specific billing document item.
*ItemPricingElementApi* | [**aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterGet**](docs/Api/ItemPricingElementApi.md#abillingdocumentitemprcgelmntbillingdocumentbillingdocumentbillingdocumentitembillingdocumentitempricingproceduresteppricingproceduresteppricingprocedurecounterpricingprocedurecounterget) | **GET** /A_BillingDocumentItemPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;) | Reads the item pricing elements for a specific item and item pricing element.
*ItemPricingElementApi* | [**aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentGet**](docs/Api/ItemPricingElementApi.md#abillingdocumentitemprcgelmntbillingdocumentbillingdocumentbillingdocumentitembillingdocumentitempricingproceduresteppricingproceduresteppricingprocedurecounterpricingprocedurecountertobillingdocumentget) | **GET** /A_BillingDocumentItemPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;)/to_BillingDocument | Reads the billing document header for a specific item and pricing element.
*ItemPricingElementApi* | [**aBillingDocumentItemPrcgElmntBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemPricingProcedureStepPricingProcedureStepPricingProcedureCounterPricingProcedureCounterToBillingDocumentItemGet**](docs/Api/ItemPricingElementApi.md#abillingdocumentitemprcgelmntbillingdocumentbillingdocumentbillingdocumentitembillingdocumentitempricingproceduresteppricingproceduresteppricingprocedurecounterpricingprocedurecountertobillingdocumentitemget) | **GET** /A_BillingDocumentItemPrcgElmnt(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,PricingProcedureStep&#x3D;&#39;{PricingProcedureStep}&#39;,PricingProcedureCounter&#x3D;&#39;{PricingProcedureCounter}&#39;)/to_BillingDocumentItem | Reads a billing document item for a specific item and item-level pricing element.
*ItemPricingElementApi* | [**aBillingDocumentItemPrcgElmntGet**](docs/Api/ItemPricingElementApi.md#abillingdocumentitemprcgelmntget) | **GET** /A_BillingDocumentItemPrcgElmnt | Reads item pricing elements of all billing documents.
*ItemTextApi* | [**aBillingDocumentItemBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemToItemTextGet**](docs/Api/ItemTextApi.md#abillingdocumentitembillingdocumentbillingdocumentbillingdocumentitembillingdocumentitemtoitemtextget) | **GET** /A_BillingDocumentItem(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;)/to_ItemText | Reads the item texts of a specific billing document.
*ItemTextApi* | [**aBillingDocumentItemTextBillingDocumentBillingDocumentBillingDocumentItemBillingDocumentItemLanguageLanguageLongTextIDLongTextIDGet**](docs/Api/ItemTextApi.md#abillingdocumentitemtextbillingdocumentbillingdocumentbillingdocumentitembillingdocumentitemlanguagelanguagelongtextidlongtextidget) | **GET** /A_BillingDocumentItemText(BillingDocument&#x3D;&#39;{BillingDocument}&#39;,BillingDocumentItem&#x3D;&#39;{BillingDocumentItem}&#39;,Language&#x3D;&#39;{Language}&#39;,LongTextID&#x3D;&#39;{LongTextID}&#39;) | Reads item texts for a specific language and long text ID.
*ItemTextApi* | [**aBillingDocumentItemTextGet**](docs/Api/ItemTextApi.md#abillingdocumentitemtextget) | **GET** /A_BillingDocumentItemText | Reads item texts of all billing documents.

## Models

- [ABillingDocumentItemPartnerType](docs/Model/ABillingDocumentItemPartnerType.md)
- [ABillingDocumentItemPrcgElmntType](docs/Model/ABillingDocumentItemPrcgElmntType.md)
- [ABillingDocumentItemTextType](docs/Model/ABillingDocumentItemTextType.md)
- [ABillingDocumentItemType](docs/Model/ABillingDocumentItemType.md)
- [ABillingDocumentPartnerType](docs/Model/ABillingDocumentPartnerType.md)
- [ABillingDocumentPrcgElmntType](docs/Model/ABillingDocumentPrcgElmntType.md)
- [ABillingDocumentTextType](docs/Model/ABillingDocumentTextType.md)
- [ABillingDocumentType](docs/Model/ABillingDocumentType.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemPartnerType](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemPartnerType.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemPartnerTypeCreate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemPartnerTypeCreate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemPartnerTypeUpdate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemPartnerTypeUpdate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemPrcgElmntType](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemPrcgElmntType.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemPrcgElmntTypeCreate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemPrcgElmntTypeCreate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemPrcgElmntTypeUpdate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemPrcgElmntTypeUpdate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemTextType](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemTextType.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemTextTypeCreate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemTextTypeCreate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemTextTypeUpdate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemTextTypeUpdate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemType](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemType.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemTypeCreate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemTypeCreate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemTypeCreateToItemText](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemTypeCreateToItemText.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemTypeCreateToPartner](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemTypeCreateToPartner.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemTypeCreateToPricingElement](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemTypeCreateToPricingElement.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemTypeToItemText](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemTypeToItemText.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemTypeToPartner](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemTypeToPartner.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemTypeToPricingElement](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemTypeToPricingElement.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentItemTypeUpdate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentItemTypeUpdate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentPartnerType](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentPartnerType.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentPartnerTypeCreate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentPartnerTypeCreate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentPartnerTypeUpdate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentPartnerTypeUpdate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentPrcgElmntType](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentPrcgElmntType.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentPrcgElmntTypeCreate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentPrcgElmntTypeCreate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentPrcgElmntTypeUpdate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentPrcgElmntTypeUpdate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTextType](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTextType.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTextTypeCreate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTextTypeCreate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTextTypeUpdate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTextTypeUpdate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentType](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentType.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTypeCreate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTypeCreate.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTypeCreateToItem](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTypeCreateToItem.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTypeCreateToPartner](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTypeCreateToPartner.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTypeCreateToPricingElement](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTypeCreateToPricingElement.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTypeCreateToText](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTypeCreateToText.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTypeToItem](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTypeToItem.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTypeToPartner](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTypeToPartner.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTypeToPricingElement](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTypeToPricingElement.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTypeToText](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTypeToText.md)
- [APIBILLINGDOCUMENTSRVABillingDocumentTypeUpdate](docs/Model/APIBILLINGDOCUMENTSRVABillingDocumentTypeUpdate.md)
- [APIBILLINGDOCUMENTSRVCancelResult](docs/Model/APIBILLINGDOCUMENTSRVCancelResult.md)
- [APIBILLINGDOCUMENTSRVFunctionImportResult](docs/Model/APIBILLINGDOCUMENTSRVFunctionImportResult.md)
- [APIBILLINGDOCUMENTSRVGetPDFResult](docs/Model/APIBILLINGDOCUMENTSRVGetPDFResult.md)
- [CollectionOfABillingDocumentItemPartnerType](docs/Model/CollectionOfABillingDocumentItemPartnerType.md)
- [CollectionOfABillingDocumentItemPrcgElmntType](docs/Model/CollectionOfABillingDocumentItemPrcgElmntType.md)
- [CollectionOfABillingDocumentItemTextType](docs/Model/CollectionOfABillingDocumentItemTextType.md)
- [CollectionOfABillingDocumentItemType](docs/Model/CollectionOfABillingDocumentItemType.md)
- [CollectionOfABillingDocumentPartnerType](docs/Model/CollectionOfABillingDocumentPartnerType.md)
- [CollectionOfABillingDocumentPrcgElmntType](docs/Model/CollectionOfABillingDocumentPrcgElmntType.md)
- [CollectionOfABillingDocumentTextType](docs/Model/CollectionOfABillingDocumentTextType.md)
- [CollectionOfABillingDocumentType](docs/Model/CollectionOfABillingDocumentType.md)
- [CollectionOfCancelResult](docs/Model/CollectionOfCancelResult.md)
- [ConditionFactor](docs/Model/ConditionFactor.md)
- [ConditionFactor1](docs/Model/ConditionFactor1.md)
- [Error](docs/Model/Error.md)
- [ErrorError](docs/Model/ErrorError.md)
- [ErrorErrorMessage](docs/Model/ErrorErrorMessage.md)
- [GetPDFResult](docs/Model/GetPDFResult.md)
- [GetPDFResultD](docs/Model/GetPDFResultD.md)
- [Wrapper](docs/Model/Wrapper.md)
- [Wrapper1](docs/Model/Wrapper1.md)
- [Wrapper2](docs/Model/Wrapper2.md)
- [Wrapper3](docs/Model/Wrapper3.md)
- [Wrapper4](docs/Model/Wrapper4.md)
- [Wrapper5](docs/Model/Wrapper5.md)
- [Wrapper6](docs/Model/Wrapper6.md)
- [Wrapper7](docs/Model/Wrapper7.md)
- [Wrapper8](docs/Model/Wrapper8.md)

## Authorization

Authentication schemes defined for the API:
### BasicAuth

- **Type**: HTTP basic authentication

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.1.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`

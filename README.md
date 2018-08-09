# amazon-mws-finances
Amazon Marketplace Web Service Finances PHP Client Library - Version 2015-05-01
=================================================

Installation
------------

Install [Composer](http://getcomposer.org/) and add amazon-mws-finances to your `composer.json`:

    composer require sherif807/amazon-mws-finances:dev-master

Version
-------

Current version is `MWSFinancesPHPClientLibrary-2015-05-01._V312120327_`.

Installation
----------
Add the reference into your composer.json : 
```
    "sherif807/amazon-mws-finances": "dev-master"
	composer update
```

```
Use in controller :

 $config = array (
   'ServiceURL' => $serviceUrl,
   'ProxyHost' => null,
   'ProxyPort' => -1,
   'ProxyUsername' => null,
   'ProxyPassword' => null,
   'MaxErrorRetry' => 3,
 );

 $service = new \MWSFinancesService_Client(
        AWS_ACCESS_KEY_ID,
        AWS_SECRET_ACCESS_KEY,
        APPLICATION_NAME,
        APPLICATION_VERSION,
        $config);

 $request = new \MWSFinancesService_Model_ListFinancialEventGroupsRequest();
 $request->setSellerId(MERCHANT_ID);
 $date = new \DateTime('today', new \DateTimeZone('UTC'));
 $request->setFinancialEventGroupStartedAfter($date->format('c'));
 $response = $service->ListFinancialEventGroups($request);
 ```
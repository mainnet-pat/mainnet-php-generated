# Mainnet

A developer friendly bitcoin cash wallet api

This API is currently in active development, breaking changes may
be made prior to official release of version 1.

**Important:** This library is in active development


This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: 0.0.2
- Build package: org.openapitools.codegen.languages.PhpClientCodegen

## Requirements

PHP 7.2 and later

## Installation & Usage

### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/mainnet-cash/mainnet-php-generated.git"
    }
  ],
  "require": {
    "mainnet-cash/mainnet-php-generated": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/Mainnet/vendor/autoload.php');
```

## Tests

To run the unit tests:

```bash
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new Mainnet\Api\ContractApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$escrow_request = new \Mainnet\Model\EscrowRequest(); // \Mainnet\Model\EscrowRequest | Request a new escrow contract

try {
    $result = $apiInstance->createEscrow($escrow_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ContractApi->createEscrow: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://rest-unstable.mainnet.cash*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ContractApi* | [**createEscrow**](docs/Api/ContractApi.md#createescrow) | **POST** /contract/escrow/create | Create an escrow contract
*ContractApi* | [**escrowFn**](docs/Api/ContractApi.md#escrowfn) | **POST** /contract/escrow/call | Finalize an escrow contract
*ContractApi* | [**escrowUtxos**](docs/Api/ContractApi.md#escrowutxos) | **POST** /contract/escrow/utxos | List specific utxos in a contract
*MineApi* | [**mine**](docs/Api/MineApi.md#mine) | **POST** /mine | Mine regtest coins to a specified address
*WalletApi* | [**balance**](docs/Api/WalletApi.md#balance) | **POST** /wallet/balance | Get total balance for wallet
*WalletApi* | [**createWallet**](docs/Api/WalletApi.md#createwallet) | **POST** /wallet/create | create a new wallet
*WalletApi* | [**depositAddress**](docs/Api/WalletApi.md#depositaddress) | **POST** /wallet/deposit_address | Get a deposit address in cash address format
*WalletApi* | [**depositQr**](docs/Api/WalletApi.md#depositqr) | **POST** /wallet/deposit_qr | Get receiving cash address as a qrcode
*WalletApi* | [**maxAmountToSend**](docs/Api/WalletApi.md#maxamounttosend) | **POST** /wallet/max_amount_to_send | Get maximum spendable amount
*WalletApi* | [**send**](docs/Api/WalletApi.md#send) | **POST** /wallet/send | Send some amount to a given address
*WalletApi* | [**sendMax**](docs/Api/WalletApi.md#sendmax) | **POST** /wallet/send_max | Send all available funds to a given address
*WalletApi* | [**utxos**](docs/Api/WalletApi.md#utxos) | **POST** /wallet/utxo | Get detailed information about unspent outputs (utxos)


## Documentation For Models

 - [BalanceRequest](docs/Model/BalanceRequest.md)
 - [BalanceResponse](docs/Model/BalanceResponse.md)
 - [Contract](docs/Model/Contract.md)
 - [ContractFnRequest](docs/Model/ContractFnRequest.md)
 - [ContractFnResponse](docs/Model/ContractFnResponse.md)
 - [ContractResponse](docs/Model/ContractResponse.md)
 - [DepositAddressResponse](docs/Model/DepositAddressResponse.md)
 - [EscrowRequest](docs/Model/EscrowRequest.md)
 - [MaxAmountToSendRequest](docs/Model/MaxAmountToSendRequest.md)
 - [MineRequest](docs/Model/MineRequest.md)
 - [ScalableVectorGraphic](docs/Model/ScalableVectorGraphic.md)
 - [SendMaxRequest](docs/Model/SendMaxRequest.md)
 - [SendMaxResponse](docs/Model/SendMaxResponse.md)
 - [SendRequest](docs/Model/SendRequest.md)
 - [SendRequestItem](docs/Model/SendRequestItem.md)
 - [SendResponse](docs/Model/SendResponse.md)
 - [SerializedSendRequest](docs/Model/SerializedSendRequest.md)
 - [SerializedWallet](docs/Model/SerializedWallet.md)
 - [Utxo](docs/Model/Utxo.md)
 - [UtxoResponse](docs/Model/UtxoResponse.md)
 - [WalletRequest](docs/Model/WalletRequest.md)
 - [WalletResponse](docs/Model/WalletResponse.md)
 - [ZeroBalanceResponse](docs/Model/ZeroBalanceResponse.md)


## Documentation For Authorization

All endpoints do not require authorization.

## Author

hello@mainnet.cash


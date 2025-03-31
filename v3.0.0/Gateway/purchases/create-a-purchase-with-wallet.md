---
title: "Create a purchase using a wallet"
slug: "create-a-purchase-with-wallet"
excerpt: ""
hidden: false
metadata: 
  image: []
  robots: "index"
createdAt: "Fri Sep 07 2018 02:14:08 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Fri Jun 14 2019 05:35:14 GMT+0000 (Coordinated Universal Time)"
---
## The wallet request object

The credentials required to make payments with a particular wallet provider vary according to the provider used. The `type` field in the wallet object determines which provider syntax is used. Currently supported wallets are:

- Apple Pay
- Masterpass
- Masterpass Express
- ZipMoney
- Visa Checkout

### Visa Checkout

| Field            | Type                                                 | Description                                                          |
| :--------------- | :--------------------------------------------------- | :------------------------------------------------------------------- |
| `type`           | String. For Visa Checkout, the value will be `VISA`. | Wallet provider identifier                                           |
| `encPaymentData` | String                                               | The Visa Checkout callid for the request                             |
| `encKey`         | String                                               | The Encrypted Key for decrypting the payment data from Visa Checkout |
| `callid`         | String                                               | The Encrypted Payment Data from the Visa Checkout request            |

### Masterpass

| Field                   | Type                                                   | Description                                        |
| :---------------------- | :----------------------------------------------------- | :------------------------------------------------- |
| `type`                  | String. For Masterpass, the value will be `MASTERPASS` | Wallet provider identifier                         |
| `checkout_resource_url` | String                                                 | The checkout_resource_url returned from MasterPass |
| `oauth_token`           | String                                                 | The oauth_token returned from MasterPass           |
| `oauth_verifier`        | String                                                 | The oauth_verifier returned from MasterPass        |

### Masterpass Express

| Field                         | Type                                                                    | Description                                             |
| :---------------------------- | :---------------------------------------------------------------------- | :------------------------------------------------------ |
| `type`                        | String. For Masterpass Express, the value will be `MASTERPASSEXPRESSV7` | Wallet provider identifier                              |
| `pre_checkout_transaction_id` | String                                                                  | The identifier representing the checkout transaction ID |

### ZipMoney

#### With an account token

| Field                 | Type                                                 | Description                |
| :-------------------- | :--------------------------------------------------- | :------------------------- |
| `type`                | String. For Zip Money, the value will be `ZIP_MONEY` | Wallet provider identifier |
| `token`               | Object                                               |                            |
| `token.account_token` | String                                               |                            |

#### With a checkout_id

| Field               | Type                                                 | Description                |
| :------------------ | :--------------------------------------------------- | :------------------------- |
| `type`              | String. For Zip Money, the value will be `ZIP_MONEY` | Wallet provider identifier |
| `token`             | Object                                               |                            |
| `token.checkout_id` | String                                               |                            |

### Apple Pay

|                     |                                                  |                                                                                                                                                                                                                     |
| :------------------ | :----------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `type`              | String. For Apple Pay, the value will be `APPLE` | Wallet provider identifier                                                                                                                                                                                          |
| `token`             | Object                                           |                                                                                                                                                                                                                     |
| `token.paymentData` | Object                                           | Data format is specified by the latest [Apple Pay documentation](https://developer.apple.com/library/archive/documentation/PassKit/Reference/PaymentTokenJSON/PaymentTokenJSON.html#//apple_ref/doc/uid/TP40014929) |

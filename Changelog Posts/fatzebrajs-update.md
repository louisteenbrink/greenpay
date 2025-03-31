---
title: "fatzebra.js update 2021-05-11"
slug: "fatzebrajs-update"
type: ""
createdAt: "Mon May 10 2021 04:22:40 GMT+0000 (Coordinated Universal Time)"
hidden: false
---
* Customer country field used to accept country name, e.g. Australia. It now expects to receive [ISO alpha2 country code](https://www.iban.com/country-codes) . The support for accepting country name will be dropped on 1st Nov.

* *fz.payment.success* & *fz.payment.error* events both return transaction data in full. See [here](https://docs.fatzebra.com/docs/payment) for details.

* *[verification](https://docs.fatzebra.com/docs/payment#transaction-data)* is provided in the transaction data payload for data integrity check.
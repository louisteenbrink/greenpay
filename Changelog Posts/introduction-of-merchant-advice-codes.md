---
title: "Introduction of Merchant Advice Codes"
slug: "introduction-of-merchant-advice-codes"
type: ""
createdAt: "Tue Nov 09 2021 11:08:06 GMT+0000 (Coordinated Universal Time)"
hidden: false
---
Schemes have introduced Merchant Advice Response Codes to provide feedback to merchants on how to retry failed transactions.

For Purchases/Authorizations and Refunds, where the transaction is declined, the field `merchant_advice_code` will be included in the response.

It is recommended that merchants review the [documentation](https://docs.fatzebra.com/docs/merchant-advice-codes-retries) and implement processes to handles this advice accordingly. Schemes and acquirers may issue or pass on fines merchants who do not respect the advice codes, especially the codes `do_not_retry` and `cancelled`.
---
title: "Tokenized Credit Cards"
slug: "tokenized-credit-cards"
excerpt: ""
hidden: false
metadata: 
  image: []
  robots: "index"
createdAt: "Mon Sep 10 2018 21:15:57 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Fri Jun 14 2019 05:35:14 GMT+0000 (Coordinated Universal Time)"
---
Tokenized Credit Cards is a method of storing your customers credit card details securely 'on file' in the Cloud Payments secure cardholder data environment.

Commonly this is used for recurring payments, however this can also be used to provide a streamlined customer experience, allowing them to save their payment details for future orders.

When a Credit Card is tokenized, the Gateway will return a token that is unique to your merchant account. To charge the Tokenized Credit Card, you should provide the card token in lieu of the other card details, and this is used when authorizing the payment.

Every Credit Card transaction within the Gateway results in the tokenization of a Credit Card, and the token is returned with every purchase request. This allows merchants to store the token after an order has been placed, or after an order has been processed in an out of band payment method (such as though Direct Post or a Hosted Payment Page).

Merchants can assign (if desired) an alias to the Tokenized Credit Card, which allows for a custom value to be associated with the Token for use when processing the payment. This allows for a merchant customer reference (such as a customer ID or number) to be used instead of the system generated token value.

Should a Tokenized Credit Card expire, you can update the record on file with a new expiry date when it is provided by the customer.

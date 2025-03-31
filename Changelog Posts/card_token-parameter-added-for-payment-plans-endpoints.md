---
title: "card_token parameter added for Payment Plans endpoints"
slug: "card_token-parameter-added-for-payment-plans-endpoints"
type: "improved"
createdAt: "Wed Feb 07 2024 21:59:22 GMT+0000 (Coordinated Universal Time)"
hidden: false
---
Previously, when creating a payment plan, that payment plan would use the customer's most recently updated credit card for payments. 

When creating a payment plan, you can now pass a `card_token` parameter along with the usual `customer` parameter to link the payment plan to the specific credit card. If a new card gets added to a customer after this point, the payment plan will still continue to use the associated credit card to process that plan.

As an example:

1. You create a customer "Zoey Zebra"
2. You add a card ending in 4242 to Zoey's customer record, it has a card token of "abcd1234"
3. You create a payment plan specifying this card token during the creation of that payment plan. The payment plan will be linked to this card.
4. Later, you add a different credit card (ending in 4111) to Zoey's account
5. The next payment will continue to use the 4242 credit card, instead of the newer 4111 card.

The endpoints that support this new parameter are `POST /v1.0/payment_plans` and `PUT /v1.0/payment_plans/{id}`.

If you provide no `card_token` when creating payment plans, the current credit card _at the time of payment_ will be used.
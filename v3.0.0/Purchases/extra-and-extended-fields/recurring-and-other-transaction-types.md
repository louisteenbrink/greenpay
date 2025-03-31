---
title: "Recurring & Other Transaction Types"
slug: "recurring-and-other-transaction-types"
excerpt: ""
hidden: false
metadata: 
  image: []
  robots: "index"
createdAt: "Thu Nov 08 2018 05:08:25 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Wed Feb 10 2021 01:48:04 GMT+0000 (Coordinated Universal Time)"
---
The ECM describes the card transaction type. The field is two digits (mn) with the possible values being:

| First Digit (m)     | Second Digit (n) |
| :------------------ | :--------------- |
| Telephone Order - 1 | Single - 1       |
|                     | Recurring - 2    |
|                     | Instalment - 3   |
| Mail Order - 2      | Single - 1       |
|                     | Recurring - 2    |
|                     | Instalment - 3   |
| Internet Order - 3  | Single - 1       |
|                     | Recurring - 2    |
|                     | Instalment - 3   |

```json Example: Single Internet Payment
{
  "extra": {
    "ecm": 31
  }
}
```

```json Example: Recurring Mail Order Payment
{
  "extra": {
    "ecm": 22
  }
}
```

 The omit expiry field set to true can also be sent through for recurring transactions against expired cards. This will allow the transaction to be sent to the banking network without the expiry date field. Typically, this field increases approval rates for recurring transactions against expired cards.

```json Example: Omit Expiry Flag
{
  "extra": {
    "omit_expiry": true,
    "ecm": 32
  }
}
```

The card-on-file field set to true can be sent through to identify transactions performed using stored payment credentials.

```json Example: Card On File Flag
{
  "extra": {
    "card_on_file": true
  }
}
```

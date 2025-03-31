---
title: "Invoices"
slug: "invoices"
excerpt: ""
hidden: false
metadata: 
  image: []
  robots: "index"
createdAt: "Sun May 13 2018 23:53:52 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Fri Jun 14 2019 05:35:14 GMT+0000 (Coordinated Universal Time)"
---
# Invoices are predefined charges that can be paid at a later date via the Hosted Payment Pages.

| Field         | Type    | Description                                          |
| :------------ | :------ | :--------------------------------------------------- |
| `amount`      | integer | Amount of the invoice in the smallest currency unit. |
| `currency`    | string  | The ISO-4217 3-letter currency code for the invoice. |
| `description` | string  | Description for the invoice.                         |
| `reference`   | string  | Your reference for this invoice.                     |
| `payable`     | boolean | Indicates whether the invoice is awaiting payment.   |

# Invoice Import Fields

| Field  | Type   | Description                        |
| :----- | :----- | :--------------------------------- |
| `uuid` | string | Unique identifier for this import. |

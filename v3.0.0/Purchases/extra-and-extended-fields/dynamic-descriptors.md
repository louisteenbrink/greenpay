---
title: "Dynamic Descriptors"
slug: "dynamic-descriptors"
excerpt: ""
hidden: false
metadata: 
  image: []
  robots: "index"
createdAt: "Thu Nov 08 2018 05:22:51 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Fri Jun 14 2019 05:35:14 GMT+0000 (Coordinated Universal Time)"
---
Specifies the card acceptor descriptor details to show up on the cardholder's statement. This is currently only supported for NAB merchants and must be enabled before use.

Dynamic Descriptors are specified by the field **descriptor** of type **Hash**.  
Required "descriptor" fields are **name** and **location** and they are both of type **String**.

| Field        | Type   | Description                                                                            |
| :----------- | :----- | :------------------------------------------------------------------------------------- |
| **name**     | String | The card descriptor name to show on the customers statement. Maximum 20 characters     |
| **location** | String | The card descriptor location to show on the customers statement. Maximum 13 characters |

```json Example: Dynamic Descriptors
{
  "extra": {
    "descriptor": {
      "name": "Biz Name Pty",
      "location": "Surry Hills"
    }
  }
}
```

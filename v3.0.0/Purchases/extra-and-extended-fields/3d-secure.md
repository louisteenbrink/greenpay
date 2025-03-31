---
title: "3D Secure Card Payments"
slug: "3d-secure"
excerpt: ""
hidden: false
metadata: 
  image: []
  robots: "index"
createdAt: "Thu Nov 08 2018 05:10:42 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Fri Jun 14 2019 05:35:14 GMT+0000 (Coordinated Universal Time)"
---
All fields should be included under the extra key in the request payload.

The values for **sli**, **xid**, **cavv**, **par** and **ver** should be supplied by the 3D Secure MPI being used for transaction authentication.

| Field name | Type              | Description                                                                                                                                                      |
| :--------- | :---------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| sli        | String (2-digits) | The Security Level Indicator (SLI) indicates the type of card holder authentication used for the transaction. Accepted values are described in the table bellow. |
| xid        | String            | The XID is the transaction ID from the 3D Secure provider. This is Base64 encoded data.                                                                          |
| cavv       | String            | The CAVV is the card authentication verification value, provided by the 3D Secure Provider. This is Base64 encoded data.                                         |
| par        | String            | This is the PARes value from 3D Secure                                                                                                                           |
| ver        | String            | This is the VERes value from 3D Secure                                                                                                                           |

| "sli" accepted values | Description                                                                                  |
| :-------------------- | :------------------------------------------------------------------------------------------- |
| "05"                  | Secure, Authenticated transaction with XID and CAVV present                                  |
| "06"                  | Secure, Non-authenticated transaction (XID present, CAVV not present)                        |
| "07"                  | Secure, Non-authenticated transaction (XID and CAVV not present). This is the default value. |
| "09"                  | Non-authenticated transaction - issuer not support. CAVV not present.                        |

Note: All fields should be included under the extra key in the request payload.

```json Example: Security Level Indicator (sli)
{
    "extra": {
        "sli": "09"
    }
}
```

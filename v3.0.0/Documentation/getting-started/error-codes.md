---
title: "Errors"
slug: "error-codes"
excerpt: ""
hidden: false
metadata: 
  image: []
  robots: "index"
createdAt: "Tue Jul 17 2018 07:35:48 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Fri Jun 14 2019 05:35:14 GMT+0000 (Coordinated Universal Time)"
---
Cloud Payments uses standard HTTP response codes to indicate success or failure of an API request. In general, codes in the 2XX range indicate success. Codes in the 4XX range indicate an error based on the information provided (e.g., a required parameter was omitted, a charge failed). Codes in the 5XX range indicate an error with Cloud Payments' systems. 

Some 4XX errors can be handled programmatically (e.g., a card is declined) and include an error code that briefly explains the error reported.

## HTTP status code summary

| Status Code                        | Summary                                                                                                                                                                                                                 |
| :--------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 200 - OK                           | The request was successfully completed.                                                                                                                                                                                 |
| 201 - Created                      | The request was successful and a transaction was created.                                                                                                                                                               |
| 400 - Bad Request                  | Bad data was received.                                                                                                                                                                                                  |
| 401 - Unauthorised                 | Your API credentials were not valid.                                                                                                                                                                                    |
| 403 - Forbidden                    | The resource you were requesting is not available for your credentials. You will most commonly see this is you are attempting to fetch a payment or refund created by your live credentials with your test credentials. |
| 404 - Not Found                    | The requested object was not found.                                                                                                                                                                                     |
| 422 - Unprocessable Entity         | The data provided was unprocessable, however the syntax of the request was correct.                                                                                                                                     |
| 500, 502, 503, 504 - Server Errors | Something went wrong with Cloud Payments' systems.                                                                                                                                                                      |

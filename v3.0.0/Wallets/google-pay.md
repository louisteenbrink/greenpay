---
title: "Google Pay™"
slug: "google-pay"
excerpt: "A faster, safer way to pay. Google Pay™ allows your customers to securely and quickly check out in apps and on the web."
hidden: true
metadata: 
  image: []
  robots: "index"
createdAt: "Thu May 23 2019 06:47:45 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Tue Jun 25 2019 11:43:09 GMT+0000 (Coordinated Universal Time)"
---
# Google Pay Checkout Workflow

- A customer adds a credit, debit, or other payment method into Google Pay. This occurs when the customer adds payment method details into the Google Pay Android or Web app, or when the customer uses a payment method to buy a Google product or service (like an app or movie on Google Play, or storage space for Google Drive).
- The customer chooses to Buy with Google Pay on the merchant's website or Android app and only needs to then select their card and shipping address.
- The merchant receives an encrypted Google Pay token and sends this to Cloud Payments. Your systems are not exposed to the PCI Scope for this data.

# Implementation Methods

There are three methods that merchants can choose from to implement Google Pay with Cloud Payments:

1. **[Android App](android-app-integration)**: integrate Google Pay into an Android application.
2. **[Web Integration](web-integration):** integrate Google Pay into your website using the Google Pay API Javascript client library.
3. **[Via Cloud Payments Hosted Payments Page](hosted-payments-page-integration)**: integrate Google Pay into your website by iframing or redirecting to the Cloud Payments Hosted Payments Page. The Cloud Payments Hosted Payments Page will then handle the Google Pay checkout flow for you.

For instructions on each implementation method, click on the relevant link above.

# Testing

To test Google Pay you must log in to a real Google account and create a Google Pay wallet with a valid card. Google does not provide a list of test cards, so a real card must be added to your wallet.

The Google Pay API will not return live, chargeable payment information in Google's test environments. The test environment can be configured on both Android App and Web Integrations - refer to Google's [About the test environment](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist#about-the-test-environment) documentation for more information.

The [Cloud Payments Sandbox environment](doc:endpoint-base-urls) will accept the non-chargeable payment information returned by the Google Pay API test environment.

| Cloud Payments Environment | Google Pay Environment   |
| :------------------------- | :----------------------- |
| Sandbox                    | `ENVIRONMENT_TEST`       |
| Production                 | `ENVIRONMENT_PRODUCTION` |

# Additional Information

## Supported Authorization Methods

| Authorization Method |
| :------------------- |
| `PAN_ONLY`           |
| `CRYPTOGRAM_3DS`     |

## Supported Card Networks

| Card Network |
| :----------- |
| `AMEX`       |
| `JCB`        |
| `MASTERCARD` |
| `VISA`       |

## Billing Address Requirements

The Cloud Payments API does not require any billing address details to be sent. This is subject to change in the future.

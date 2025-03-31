---
title: "Changes to Direct Entry Descriptions"
slug: "changes-to-direct-entry-descriptions"
type: ""
createdAt: "Thu Sep 03 2020 02:52:03 GMT+0000 (Coordinated Universal Time)"
hidden: true
---
In order to improve the reliability of Direct Entry rejection matching and to improve the quality of descriptions for debits or credits in customer's bank statements we are updating the validation rules for the creation of Direct Entries (i.e. Direct Debits and Direct Credits) to enforce uniqueness on the description field.

From the 7th of September, 2020 any new merchants will be required to meet this new requirement. If a record is created where the uniqueness constraint is not met an error will be returned and the record will not be saved.

For any merchants existing prior to this date the changes will not be hard-enforced, however there will be a soft-enforcement applied - this means that if a record is created where the description field is not unique it will be updated before being saved to include a unique value at the end. This may result in truncation of the value provided in the request. The response from our system will include the updated value if this case is applicable.
[block:callout]
{
  "type": "info",
  "title": "How will my descriptions change?",
  "body": "If you have provided a generic description which does not meet uniqueness constraints (for example: 'Invoice' or 'Payment') we will modify this to include a randomly generated value:\n\n'Invoice' becomes 'Invoice*ABC123'\n\nIn the event that the value you provided is greater then 11 characters long the value provided will be truncated to include the random value:\n\n'Invoice Payment' becomes 'Invoice Pay*ABC123'"
}
[/block]
We wish to encourage all merchants to update their systems to provide a unique, descriptive value, if possible, however we understand that making these changes is not always possible, which is why we have taken this approach.

If there are any questions, comments or concerns please feel free to contact our support team for assistance.
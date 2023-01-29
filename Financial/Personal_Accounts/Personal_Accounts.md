## Personal Accounts

**Personal Accounts** define accounts into which customers can deposit money at the POS to save for future purchases in the store. For example, customers can deposit money into their Christmas Savers account, and at the end of the year receive a voucher on the accumulated amount plus an extra 5% to spend in the retailer's stores.

Money can be deposited into either EPS/Bank accounts or Loyalty accounts. When depositing into an EPS Bank Account, the customer is required to swipe their bank card to identify the account into which they are depositing after completing the tender information.

When depositing into a Loyalty account, the Loyalty card is swiped after selecting the Loyalty account.

Both processes can be performed during a sales transaction, or standalone.

**Reference Path:** *Financial/Personal Accounts/Personal Accounts*

![Personal Accounts Screen](/Images/PersonalAccountsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Account ID**|The name of the account, e.g., Holiday Savers.|
|**Account Description**|A description of the account. The description can be in multiple languages.|
|**Provider**|The service provider used to validate the customer account and payment details.|

**Reference Path:** *Financial/Personal Accounts/Personal Accounts/Add New*

![Personal Accounts Form](/Images/PersonalAccountsForm.png)

|**Field**|**Description**|
|---------|----------|
|**Account ID**|The Account ID.|
|**Account Description**|A description of the account, e.g., Holiday Savers. This is a mandatory field, and the description must be unique.|
|**Provider**|The service provider used to validate the customer account and payment details.<BR>The options are:<BR><BR>**Loyalty** - used to validate the customer account details. When the customer's member card is scanned, the system sends the details to the Loyalty provider. Once validated, the provider sends the account name, customer name, and account balance to the POS.<BR>**EPS** - Used to authorize payment when an EFT or Gift Card is used to deposit money into the Personal Account.<BR>**Note:** More than one account can be defined with the same Account Name, however, each account must have a different provider. The same provider cannot be used for accounts with the same Account Name.|
|**Basic Definitions**|
|Display Account Balance|Indicates if the current account balance is displayed at the POS when the customer wants to deposit money to the account. The current balance does not include the current amount the customer wants to deposit.|
|**Item & Tender Settings**|
|Item|The product to which the personal account is associated, for example Deposit EPS.<BR>Each personal account is associated with a dedicated product. The tender restrictions defined for the personal account are defined as a Tender Item Restriction on the dedicated item.|
|External ID|The external ID number assigned to the selected item.|
|Tender|The tender allowed to deposit money into the selected account. This is a mandatory field.|
|Minimum Amount|The minimum amount that can be deposited by the customer into the account using the selected tender. If no amount is specified, there is no minimum.|
|Maximum Amount|The maximum amount that can be deposited by the customer into the account using the selected tender. If no amount is specified, an unlimited amount can be deposited.|
|Message|The error message displayed in the event of an amount violation.|
|**Deposit Threshold Settings**|Defines the thresholds limiting the amount customers can deposit in a personal account during a retail transaction. If a customer wants to deposit an amount which exceeds the defined threshold, a message is displayed informing the cashier of the action required. For example, you can prohibit deposits of more than $2000.00 or require the manager to approve the deposit amount.<BR>Only the tenders selected in the Tender field can be used to deposit money into Personal Accounts.|
|From Amount|The minimum amount that can be deposited in a personal account. If no amount is specified, there is no minimum amount.|
|To Amount|The maximum amount that can be deposited in a personal account. If no amount is specified, there is no maximum amount.|
|Action|The action required when the amount deposited in the personal account exceeds the defined threshold amounts.<BR>The options are:<BR><BR>**Prohibit** - the deposited amount is not allowed.<BR>**Allow with Manager Approval** - the deposited amount requires manager approval.|
|Roles|The role that must be assigned to the user who approves the deposit amount, when manager approval is required.|
|Messages|**TenderAmountViolation** - The message displayed at the POS when the amount deposited exceeds the defined thresholds.|
## Tender Exchange

**Tender Exchange** defines the tenders which can be purchased and paid with another tender, e.g., pay with Visa and get cash. For example, a customer may have purchased items and paid with cash, and then realize that they need the cash. The customer can then request to pay with a different tender, e.g., Visa. The cashier performs a tender exchange to replace the cash tender recorded in the ticket with the Visa tender that the customer wants to use.

There are various business motivations for Tender Exchange. For example:

* Cash withdrawal services from ATM machines - Customer pays with an EFT card and gets a refund with cash.
* Tender correction – Customers pay with Visa for Goods and want to swap the payment with a different payment mean

**Reference Path:** *Financial/Tendering/Tender Exchange*

![Tender Exchange Screen](/Images/TenderExchangeScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the Tender Exchange.|

**Reference Path:** *Financial/Tendering/Tender Exchange/Add New*

![Tender Exchange Form](/Images/TenderExchangeForm.png)

|**Field**|**Description**|
|---------|----------|
|**ID**|The Tender Exchange ID.|
|**Name**|The description of the tender exchange.|
|**Cashout**|Indicates if a Gift Card balance can be exchanged for cash. For example, if set to Yes, a Gift Card with a balance of $50.00 can be exchanged for $50.00 in cash. This option is relevant only to Gift Card tenders.<BR>**Note:** When a Gift Card is configured to allow Cashout, the system does not validate the values defined in the Minimum Amount, Maximum Amount, and Multiples Of fields.|
|**Minimum Amount**|The minimum amount that can be exchanged using the selected tender. For example, if the customer paid $10.00 for a transaction in cash, and they want to exchange the payment to credit card, but the minimum amount defined is $25.00, the cashier cannot give the customer the cash back.|
|**Maximum amount**|The maximum amount that can be exchanged using the selected tender.  For example, if the customer paid $50.00 for a transaction in cash, and requests to rather pay the $50.00 by credit card, and the maximum amount defined is $25.00, the cashier cannot give the customer $50.00 back in cash.|
|**Multiples Of**|The lowest denomination allowed for the tender exchange. Amounts purchased or refunded must be multiples of the lowest denomination. For example, if the lowest denomination is 5, the customer can only exchange amounts of $5.00, $10.00, $15.00 and so on.|
|**Refund Tenders**|The tender given to the customer in the tender exchange. For example, Cash.|
|**Pay with Tenders**|The tender used to pay for the tender exchange from the customer, e.g., credit card.|

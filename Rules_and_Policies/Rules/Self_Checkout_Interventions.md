## Self Checkout Interventions

**Self Checkout Interventions** configure interventions defined for the Self Checkout. Interventions are a type of alert indicating that there is a problem and the shopper needs help to continue with their transaction, or an issue that the shopper must acknowledge in order to continue with their transaction.

Interventions can be either:

* **Immediate** – When the intervention is triggered, it must be handled immediately and the shopper cannot continue shopping until the Intervention is resolved. The tower light turns red to notify the attendant.
* **Delayed** – When the intervention is triggered, the shopper can continue to shop until the shopper selects Finish & Pay, and then all the delayed interventions become immediate and the required action must be performed to clear the intervention by the attendant. This enables the attendant to handle all the interventions that occurred during the transaction all at once, reducing the number of times that the attendant has to approach the lane, and saving the shopper time. 
Delayed interventions turn the tower light yellow and can be handled at any time during the transaction before the shopper selects Finish & Pay, using the Go To POS function. If the intervention is not solved before the shopper selects Finish & Pay, it becomes an immediate intervention when Finish & Pay is selected and the tower light turns red to notify the attendant.
* **Ignored** - The intervention is ignored and not triggered.

Interventions can be handled by either the shopper or the attendant depending on the type of Intervention and its configuration.

Each intervention can be configured to suit your business needs. There are a combination of different configuration options, for example:

* Immediate intervention that requires an attendant to intervene and solve the issue
* Immediate intervention that requires an attendant to acknowledge the issue
* Immediate intervention that the shopper can acknowledge and continue with their transaction
* Delayed intervention that requires an attendant to solve the issue
* Ignored intervention where the intervention is ignored and not triggered

When an attendant is required to intervene, the attendant performs a function called GO TO POS. This function enables the attendant to log in to the POS touchpoint from the Self Checkout, handle the problem and easily transfer back to the Self Checkout. For example, this is required for functions that the shopper is not allowed to perform, e.g., a Void, Price Override, Price Entry function.

Interventions are predefined, however, specific parameters can be modified.

Each intervention and all its configuration options are described in the Self Checkout Configuration Processes section.

**Reference Path:** *Rules & Policies/Rules/Self-Service*

![Self Checkout Interventions Screen](/Images/SelfCheckoutInterventionsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Rule/Business Error name**|The Rule or Business Error name used to describe the Self Checkout intervention. The following Self Checkout interventions are defined:<BR><BR>**Own Bag Limits Exceeded** - this intervention is triggered when to number of bags placed on the Security Sale by the shopper exceeds the defined limit.<BR>**Item Not Found** - this intervention is triggered when an item scanned by the shopper at the Self Checkout is not found in the store item catalog.<BR>**Price Entry Required** - this intervention is triggered when an item scanned by the shopper at the Self Checkout requires the shopper to manually enter the item's price.<BR>**Price Verify** - this intervention is triggered when an item scanned by the shopper at the Self Checkout requires the shopper to check the item's price.<BR>**Electronic Item Scanned Without Serial Number** - this intervention is triggered when an electronic item is scanned at the Self Checkout and the shopper is required to enter a serial number.<BR>**Invalid Loyalty** - this intervention is triggered when an invalid loyalty card is scanned by the shopper.<BR>**Tender Declined** - this intervention is triggered when the tender selected to pay for the transaction is not accepted.<BR>**EPS Declined** - this intervention is triggered when the shopper tries to pay with a credit card which is not approved.<BR>**EPS Needs More Parameters** - this intervention is triggered when additional information is required when a credit card is scanned to pay for the transaction, e.g., the PIN number.<BR>**Online Activation Failed** - this intervention is triggered when the shopper scans a Gift Card and the card is not activated by the provider.<BR>**Gift Card Not Recognized** - this intervention is triggered when a Gift Card that is not identified by the system is scanned by the shopper.<BR>**Locked For Sale** - this intervention is triggered when an item that is prohibited for sale is scanned by the shopper.<BR>**Coupon Accepted at SCO** - this intervention is triggered when a coupon is scanned and the attendant must collect the coupon.<BR>**Coupon Declined Due to Coupon Rules** - this intervention is triggered when a coupon that does not meet the specified coupon rules is scanned, e.g., the coupon has expired.<BR>**Coupon Manual Entry Required** - this intervention is triggered when a coupon is scanned by the shopper and the coupon amount must be manually entered.|

**Reference Path:** *Rules & Policies/Rules/Self Checkout Interventions/Add New*

![Business Error Screen](/Images/BusinessErrorScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Business Error**|The intervention name.|
|**Locations List**|The locations the rule is applied to.|
|**Action**|The action required to clear the intervention triggered at the Self Checkout t the selected Location. Only actions which can be modified for the selected intervention are enabled.<BR>Action settings are only active at the locations where the rule is active.|
|Attendant required|Indicates that the shopper cannot continue with the transaction until an attendant clears the intervention.|
|Delayed intervention|Indicates that the intervention does not require immediate handling and the shopper can continue scanning until they select the Finish & Pay button.<BR>It then becomes an immediate intervention, and the required action must be performed to clear the intervention by the attendant.|
|Ignore intervention|Indicates that the intervention is not triggered, and the shopper can continue shopping.|
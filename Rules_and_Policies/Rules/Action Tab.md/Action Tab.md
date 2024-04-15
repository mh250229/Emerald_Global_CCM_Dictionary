### Action Tab

The Action Tab defines the action taken when a business rule is triggered. A message is always displayed, and additional user or cashier action may be necessary. 

**Reference Path:** *Rules & Policies/Rules/Business Rules/Add New/ Action Tab*

![Action Tab](/Images/ActionTab.png)

The following Action types are supported:

* Member Validation
* Prohibit
* Approval required
* Select reason
* Enter loyalty card
* Prompt for confirmation
* Form
* Input date required
* Notification

#### Action Types

##### Member Validation

The Member Validation action is used to validate Loyalty members who request to pay or partially pay for their transaction with ‘Points’.  
The Member Validation action type is used for the payment BRM.

![Member Validation](/Images/MemberValidation.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Member Validation|
|**Message**|The message prompting the customer/cashier that the action is prohibited.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|
|**Input Label**|Defines the text title above the message input fields. For example, if a Date is selected from the Input Type drop-down list, and the cashier is required to enter the date of birth for a customer, the input label may be: Enter the date (DD/MM/YYYY).|
|**Validate By**|Specifies how the loyalty member validated. The options are:<BR>Date of Birth<BR>4 last digits of ID|
|**On Self Checkout**|Specifies how the Business Rule/Intervention is handled on the Self Checkout.<BR>The options are:<BR>**Requires attendant** - indicates that an attendant is required to resolve the intervention.<BR>**Triggered as delayed** – indicates if the intervention is handled immediately or is delayed so that the attendant can handle the intervention anytime during the transaction.<BR>If selected, the intervention is delayed and the shopper can continue shopping. Once the shopper finishes scanning their items and selects the Finish & Pay button, and the attendant has not yet handled the intervention, it then becomes an immediate intervention and the required action must be performed by the attendant to clear the intervention .<BR>If not selected, the intervention must be handled immediately. The shopper cannot continue shopping until the intervention is resolved.|

##### Prohibit

The **Prohibit** Action Type restricts certain items, or groups of items from being sold on a specific touchpoint, or prevent specific functions, etc. which are part of a business rule.  

![Prohibit](/Images/Prohibit.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Prohibit|
|**Message**|The message prompting the customer/cashier that the action is prohibited.|
|**On Self Checkout**|Specifies how the Business Rule/Intervention is handled on the Self Checkout.<BR>The options are:<BR>**Requires attendant** - indicates that an attendant is required to resolve the intervention.<BR>**Triggered as delayed** – indicates if the intervention is handled immediately or is delayed so that the attendant can handle the intervention anytime during the transaction.<BR>If selected, the intervention is delayed and the shopper can continue shopping. Once the shopper finishes scanning their items and selects the Finish & Pay button, and the attendant has not yet handled the intervention, it then becomes an immediate intervention and the required action must be performed by the attendant to clear the intervention.<BR>If not selected, the intervention must be handled immediately. The shopper cannot continue shopping until the intervention is resolved.|

##### Approval Required

The **Approval Required** Action Type requires the manager to approve the transaction before the cashier can continue.

![Approval Required Screen](/Images/ApprovalRequiredScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Approval required|
|**Message**|The message prompting the customer/cashier that the action requires supervisor/attendant/customer approval.|
|**Roles**|The role indicating the privileges required by the person who is approving the activity.|
|**Display Confirmation Message for Approved Roles**|Specifies if a confirmation message is displayed on the POS when the user logged in to the POS is assigned to one of the approved roles when the BRM is triggered. If the rule is triggered and the user logged in to the POS is not assigned to an approved role, the Approval message is prompted.|
|**Message**|The confirmation message prompted at the POS when the user logged in is assigned to one of the approved roles.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|
|**On Self Checkout**|Specifies how the Business Rule/Intervention is handled on the Self Checkout.<BR>The options are:<BR>**Requires attendant** - indicates that an attendant is required to resolve the intervention.<BR>**Triggered as delayed** – indicates if the intervention is handled immediately or is delayed so that the attendant can handle the intervention anytime during the transaction.<BR>If selected, the intervention is delayed and the shopper can continue shopping. Once the shopper finishes scanning their items and selects the Finish & Pay button, and the attendant has not yet handled the intervention, it then becomes an immediate intervention and the required action must be performed by the attendant to clear the intervention.<BR>If not selected, the intervention must be handled immediately. The shopper cannot continue shopping until the intervention is resolved.|

##### Select Reason

The **Select Reason** Action Type requires the user to select a reason the activity was performed, before continuing with the transaction.  
For example, the cashier may be required to enter a reason when performing Price Overrides, Tax Exemptions, Open Drawer, and so on, at the POS.

![Select Reason Screen](/Images/SelectReasonScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Select reason|
|**Reason Codes**|The list of reasons from which the user can select, indicating the reason for having performed a certain activity.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|
|**Message**|The message prompting the customer/cashier that the action requires supervisor/attendant to select a reason and why.|

##### Enter Loyalty Card
The **Enter Loyalty Card** Action Type requires the requires the cashier to enter the customer's loyalty card information.

![Enter Loyalty Card Screen](/Images/EnterLoyaltyCardScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Enter Loyalty Card|
|**Message**|The message prompting the cashier to enter the Loyalty card details|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|


##### Prompt For Confirmation

The **Prompt For Confirmation** Action Type requires the user to confirm the message by selecting Yes or No before continuing with the transaction.

![Prompt For Confirmation Screen](/Images/PromptForConfirmationScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Prompt for Confirmation|
|**Message**|The message prompted to inform the cashier that confirmation is required.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|

##### Form

The **Form** Action Type requires the cashier to select a form and enter the relevant information.

![Form Screen](/Images/FormScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g. Form|
|**Form Name**|The form displayed when the business rule is triggered. This field is mandatory. All the forms are predefined forms defined by the retailer.<br>The options are:<br>**Customer Data** - to prompt a form that includes fields to enter  the Customer name and Customer phone number<br>**Table Number** - to prompt a form that includes a field to enter the table number.<br>**Configurable Form** – to prompt a form that was configured by the retailer with their own retailer data. It provides 3 fields, 2 of which are mandatory when this form is used. This configuration can be changed.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<br>**Request** - indicates that the business rule is always triggered.<br>**Transaction** - indicates that the business rule is only triggered once per transaction.|

##### Input Data Required

The **Input Data Required** Action Type requires the user to enter information in order to continue with the transaction.

![Input Data Required Screen](/Images/InputDataRequiredScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Input Data Required|
**Message**|The message prompting the customer/cashier that the action requires input.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|
|**Input Label**|Defines the text title above the message input fields. For example, if a Date is selected from the Input Type drop-down list, and the cashier is required to enter the date of birth for a customer, the input label may be: Enter the date (DD/MM/YYYY).|
|**Input Name**|Defines the name of the input message fields. This is a free text field, and you can enter a name to reflect the message displayed. For example, if a Date is selected from the Input Type drop-down list, and the cashier is required to enter the date of birth for a customer, the input name may be: Customer's Birthday|
|**Input Type**|Allows the user to enter data when a message linked to this option is triggered. The user can select the type of data they plan to enter when the message is triggered: The options are: Text, Numeric, Yes/No, Date, Birthday|
|**Max Time Period**|The maximum duration period during which online items can be activated, calculated from the current date. The cashier is able to activate an item with an activation date any time from the starting day until the maximum defined date.|
|**Time Period**|The time period is defined for either days or months.|

##### Notification

The **Notification** Action Type prompts a message informing the user but enables the user to continue with the transaction.

![Notification Screen](/Images/NotificationScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Notification|
|**Message**|The message prompted to notify the cashier.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.|

##### Enter Salesperson

The **Enter Salesperson** Action Type prompts the cashier to scan the salesperson’s barcode when adding a salesperson to the transaction.

Salespersons are employees who help customer purchases items. Retailers can reward the salesperson with a sales commission.

![Enter Salesperson Screen](/Images/EnterSalespersonScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Type**|The selected action type, e.g., Enter Salesperson|
|**Message**|The message prompted to notify the cashier to scan the Salesperson’s barcode.|
|**Scope**|Defines how often the business rule can be triggered. The options are:<BR>**Request** - indicates that the business rule is always triggered.<BR>**Transaction** - indicates that the business rule is only triggered once per transaction.<BR>**Note:** The Scope field only defines the number of times the BRM is triggered in the transaction. If Scope is set to Transaction, the salesperson is only linked to the first item scanned in the transaction that triggered the BRM and not to all the items in the ticket.|
|**Mandatory**|If selected, the cashier must scan or enter the Salesperson’s barcode in the message screen prompted when the BRM is triggered. The items cannot be sold until the cashier adds the salesperson.<BR>An error message is prompted if the cashier closes the message screen without scanning the salesperson’s barcode or enters an invalid salesperson.<BR>If not selected, the cashier can close the message screen without scanning the salesperson’s barcode, and the item is not sold.|
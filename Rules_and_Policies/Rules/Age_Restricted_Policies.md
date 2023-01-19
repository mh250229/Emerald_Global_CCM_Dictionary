## Age Restricted Policies

Age Restricted Policies enable you to define different policies for age restricted items. Age Restricted policies comprise of a set of restrictions based on the date and time items are sold, the customers age, and user age. There is no relation between the different restrictions.

For example, you can define Age Restricted policies to:

* Restrict the sale of alcohol or DVDs to customers under 18. If a customer under 18 tries to purchase one of the items the sale is prohibited.
* Prohibit the sale of age restricted items on the 25.8.2012. If a customer tries to purchase one of the items on the 25.8.2012, the sale is prohibited. However, the items can be purchased from the 26.8.2012.

In addition, once a transaction is saved and then recalled, the restricted items require approval even if they were already approved before saving the transaction.

**Reference Path:** *Rules & Policies/Rules/Age Restricted Policies*

![Age Restricted Policies Screen](/Images/AgeRestrictedPoliciesScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Policy ID**|The Age Restriction Policy ID number. The ID is unique, and can contain alphanumeric characters.|
|**Location**|The store/s or store hierarchy in which the age restriction policy is applied.|

**Reference Path:** *Rules & Policies/Rules/Age Restricted Policies/Add New*

![Age Restricted Policy Form](/Images/AgeRestrictedPolicyForm.png)

|**Field**|**Description**|
|---------|----------|
|**Policy ID**|The Age Restriction Policy ID number. The ID is unique, and can contain alphanumeric characters.|
|**Location**|The store/s or store hierarchy in which the age restriction policy is applied.|
|**Touchpoint Group Type**|The Touchpoint Group type, either Primary or Secondary, assigned to the Age Restriction rule. The options are:<BR>**Pimary** – indicates that the Age Restricted Policy can only be applied to a Primary Touchpoint Group. On selecting this option, a list of Primary Touchpoint Groups only is displayed in the Touchpoint Group option.<BR>**Secondary** - indicates that the Age Restricted Policy can only be applied to a Secondary Touchpoint Group. On selecting this option, a list of Secondary Touchpoint Groups only is displayed in the Touchpoint Group option.<BR>This enables retailers to apply Age Restriction rules to specific stores by associating touchpoints in the store to a secondary touchpoint group, and assigning the rules to the secondary touchpoint.<BR>For example, the retailer wants to prohibit selling alcoholic drinks in the store after 10 pm, and allow alcoholic drinks to be sold at the Italian venue until 11.00pm. The touchpoints in the store are linked to a Primary Touchpoint Group. In addition, the Touchpoints in the Italian Venue are assigned to a Secondary Touchpoint Group.<BR>The retailer defines a rule restricting the sale of alcoholic drinks after 10.00 pm, and assigns the rule to the Primary Touchpoint Group.<BR>The retailer defines another rule restricting the sale of alcoholic drinks after 11.00 pm, and assigns the rule to the Secondary Touchpoint Group.<BR>If the customer orders a beer at the Italian Venue at 10.30 pm. The rule is not triggered.<BR>**Note:** If the same Age Restricted Policy is applied to both a Primary and Secondary Touchpoint Group, the policy is applied to the Secondary Touchpoint Group.<BR>If the same Age Restricted Policy is applied to two different Touchpoint Groups that are associated to the touchpoint, the following strategy is applied as the fallback strategy (in the following order):<BR>The Secondary Touchpoint wins over the Primary Touchpoint Group.<BR>The Touchpoint Group with the higher ID wins over the Touchpoint Group with the lower ID.|
|**Delay Message in Self Checkout**|Indicates that the intervention is delayed and triggered only once the shopper has completed scanning their items and selected the Pay button. This enables the attendant to handle the intervention at the end of the transaction.|
|**Applies Also for Return Item**|Indicates that the age restriction policy is also applied when age restricted items are returned. This enables the cashier to decline the return of an item that was restricted when purchased.<BR>For example, if the customer is under age (under 21) and the sale of alcohol is restricted in the sale, and then a customer under the age of 21 returns an alcoholic item, the rule is applied.|
|**Policy Members**|Defines the item group linked to the Age Restriction Policy. When an item linked to the selected item group is scanned at the POS terminal, the rule is triggered and the Restriction Policy is applied. You can select one or more item groups.|
|Products & Categories|The items restricted for sale in the Age Restriction Policy.|
|Groups|The item groups restricted for sale in the Age Restriction Policy.|
|**Date/Time**|Defines Age Restriction Rules based on the date and time the items are sold. You can define an existing age restriction policy to apply from a certain date and time in the future. This enables the chain to get notice of changes to selling restricted items in advance.<BR>For example, the current date is May 1st, 2012 and on June 20th 2012 specific items are prohibited for sale. You can define the policy to take effect from June 20th 2012.<BR>**Note:** It is recommended to define time restrictions for the Kiosk using the PLU Available Hours module.|
|Action Type|The action taken when a Date Time rule is triggered at the POS terminal. Different actions can be taken for different restriction rules. The options are:<BR>**Prohibit** - the item is prohibited for sale, and cannot be added to the ticket<BR>**Approval Required** - the item can be sold only after the manager approves the sale.<BR>**Note:** When Approval Required is selected, the Roles field is enabled, and you must select the Roles that must be assigned to the user who approves the item sale, e.g., Manager Supervisor.|
|Days of the Week|To restrict the sale of items on a specific weekday.|
|Start Date / End Date<BR>No End Date|To restrict the sale of items in a specific date range.<BR>Disables the end date.|
|Start Time / End Time<BR>No End Time|To restrict the sale of items at a specific time.<BR>Disables the end time.|
|Message|The message displayed when the restriction rule is triggered. Messages are defined in the Messages module. Only messages defined for restriction rules can be selected.|
|Roles|The roles with permissions to approve the sale of the restricted item. Users must be assigned to at least one of the roles to approve the sale of the restricted item. For example, you can specify that only managers or supervisors can approve a restricted sale.|
|**User Age**|Rules based on the cashier's age.|
|Action type|The action taken when a user age rule is triggered at the POS terminal. Different actions can be taken for different restriction rules. The options are:<BR>**Prohibit** - the item is prohibited for sale and is not be added to the ticket<BR>**Approval Required** - the item can be sold only after the manager approves the sale.<BR>**Note:** When Approval Required is selected, the Roles field is enabled, and you must select the Roles that must be assigned to the user who approves the item sale, e.g., Manager Supervisor.|
|User age is less than|The minimum required cashier age.|
|Message|The message displayed when the restriction rule is triggered. Messages are defined in the Messages module. Only messages defined for restriction rules can be selected.|
|Approval Roles|User roles required to approve the sale of the restricted item once the rule is triggered. For example, managers or supervisors are required to approve a restricted sale. You can select more than one role.
|**Customer Age**|Rules based on the customer's age.|
|Cashier must enter customer’s age for each item.|The cashier is prompted to verify the customers age every time an item in one of the product groups linked to the age restriction policy is scanned. The system validates the age restriction separately for each item in the group.<BR>For example, some items, e.g., DVDs, are associated to different ages, and an Age Restriction rule cannot be defined for each item. All the DVDs are linked to the same product group which is linked to the Age Restriction Policy. When a DVD is scanned, the system validates the age restriction for the scanned DVD.<BR>Or <BR>When ordering a Happy Hour meal that includes an alcohol item that is the default drink item, or a Combo meal that includes an alcohol item that is not the default drink item.<BR>On selecting the meal, the cashier must select a drink. If the customer selects an alcohol drink, e.g., beer or wine, the Age Restriction is triggered on the whole meal, and the cashier must verify the customer's age.<BR>**Note:** When the Prompt for customer age for each item checkbox is selected. the Attribute, and Action fields are disabled.|
|Age Confirmation Action Type|The action taken when a customer age rule is triggered at the POS terminal. Age Confirmation is displayed by default and cannot be modified. The cashier is required to confirm the customer's age. The options are:<BR>**Approve / Reject** - the cashier is required to approve or reject that the customer is older than the specified age.<BR>**Enter Date of Birth / Approve / Reject** - the cashier is required to approve or reject that the customer is older than the specified age or enter the customer's birthdate to enable the system to validate that the customer's age is older than the specified date.<BR>**Note:** The date format dd/mmm/yyyy is not supported in Age Verification messages. The user cannot enter digits and characters for example, 05/Feb/2014 is not supported.<BR>**Note:** The cashier is only required to approve or reject the customer's age once in a transaction. Once the cashier approves or rejects that the customer is above X years old, all additional items that belong to the same policy and with a minimum required age of X years or less are automatically approved or rejected.<BR>For example: The customer purchases 3 items: a knife, a DVD and an alcoholic drink where all of the three require a minimum age of 18 years old in order to be purchased. Once the cashier approves the first item, the other two are approved automatically.|
|User age is less than|The minimum required customer age.|
|Message|The message displayed when the restriction rule is triggered. Messages are defined in the Messages module. Only messages defined for restriction rules can be selected.|
|Message for Automatic Reject|The message displayed when an age restricted item that was previously scanned in a transaction is re-scanned, and the system has already identified that the customer is below the required age.<BR>The cashier is not required to check the customers age. The selected message is automatically displayed and the item is automatically rejected.|
|Customer Display Message|The message displayed on the Customer Display when the restriction is triggered. The message notifies the customer that they are required to show their ID.<BR>**Note:** The message is different to the message displayed on the POS Display when an Age Restriction rule is triggered.<BR>Messages are defined in the Messages module. Only messages defined for restriction rules can be selected.|
|Reject Reason Codes|Predefined reasons indicating why the sale was rejected. Once the Customer Age rule is triggered and the sale is rejected, a list of the selected Reject Reason Codes is displayed at the POS and the cashier can select the relevant reason.<BR>This is not a mandatory field.<BR>**Note:** When the cashier selects Reject and no Reject Reason Codes are selected, the POS displays the EJ and the cashier can continue to perform transactions.|
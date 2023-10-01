## Activities

**Activities** is used to perform different cash office activities in each store for the different touchpoints during trading hours. For example, add money to a touchpoint, pay out a sum of money, etc. Each activity either increases or decreases the store balance.

**Reference Path:** *Cash Office/Business Periods/Activities*

![Activities Screen](/Images/ActivitiesScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The stores in which the cash office activities are performed.|
|**Business Date**|The Business Date on which you want to perform the Cash Office Activity. Activities cannot be performed on a date in a closed Business Period.<br>The current business date is displayed by default.<BR>To enter a date, click ![Calendar icon](/Images/calendar.png)  in the field. The calendar is displayed. Select the relevant date, and click OK.<BR>**Note**: Users without permissions are prohibited from performing Cash Office Activities for a date prior to the current business date.<BR>Configuration is via the ProhibitedRolesForPastDatesInCashOfficeActivities parameter in the OfficeBusinessConfigurationMaintenanceRequest RTI.<BR>When a user assigned to a Role that is prohibited from performing Cash Office Activities on a past date, the Business Day calendar only displays the current calendar date as defined in the system. Past dates are disabled.|
|**Tender Loan**|To define the money that is used as change at the POS/Till. This is performed at the beginning of a new period. A sum of money is transferred from the Safe to the accountability of the POS terminal. The Add Loan (Float) enables cashiers to return change to customers during trading.|
|**Tender Pickup**|To pick up money from the POS terminal and record it in the system.<br>Money is picked up for various reasons, such as End of Shift, or to prevent excessive amounts of money accumulating in the cash drawer during trading.|
|**Till Declaration**|To declare all the money from the POS touchpoints.|
|**Paid In**|To record money from an outside source, other than direct sales. For example, rent received. The money is transferred to the safe or to a till, automatically increasing the In-Safe totals.|
|**Paid Out**|To record money payments made from the Store's safe or from one of the tills, and given to an outside source for goods or services. For example, a Window Cleaner would be paid for services via a Payout transaction. Performing a Payout automatically decreases the In Safe totals.|
|**Bank Deposit**|To record money transferred money from the safe to the bank, automatically decreasing the In-safe totals.|
|**Bank Receipt**|To record money that was received from the bank, automatically increasing the In-safe totals. Once a Receipt has been recorded, the accountability of the money is transferred to the Safe.|
|**Safe Transfer**|To record money transferred from one safe to another safe.
|**Safe Declaration**|To declare the money in the safe. Only Tenders defined as Safe Declaration tenders, e.g., Cash, can be declared.
|**From Account**|The account from which money is transferred. For example, a Tender Pickup is transferred from the Store Till account.<br>Only active accounts, i.e., accounts linked to active Account Profiles can be selected.<br>**Note:** This field is not displayed for Till Declaration and Safe Declaration activities.|
|**To Account**|The account to which money is transferred. For example, a Tender Pickup is transferred to the Store Safe account.<BR>Only active accounts, i.e., accounts linked to active Account Profiles can be selected.<BR>**Note**: If there are accounts associated to Income and Expense Accounts, all the Cash Office accounts are displayed in the To Account drop-down list. However, only the associated Paid In or Paid Out accounts can be added to the Transaction List.<BR>If an unassociated Paid In or Paid Out account is selected, the following message is prompted, ‘The selected financial account is not valid for the selected Till or Safe types. Please make a different account selection’.<BR>See also: Account Profiles|
|Reference|The activity reference for each cash office activity performed in the store. This is a free text field and can contain up to 40 characters.|
|**Additional Info**|Displays additional information relevant to Cash Office Activities, for example, the name of a second cashier who counted the Safe amounts in a Bank Deposit.<BR>This field is displayed based on the configuration of the **AdditionalInfo** parameter in the CashOfficeActivityConfigurationMaintenanceRequest RTI.<BR>The configuration options are:<BR>* Optional – the Additional Info field is displayed as optional.<BR>* Mandatory - the Additional Info field is displayed as mandatory.<BR>* Not Required - the Additional Info field is not displayed.|
|Pick Account|The account for which the is performed. For example, a safe declaration can be performed on the Main Safe Account.<br>**Note:** This field is displayed only for Till Declaration and Safe Declaration activities.|
|**Transaction List**|Displays the details of the cash office activity transaction.|
|Transaction ID|The Transaction ID number of the selected Cash Office Activity. The system automatically assigns the Transaction ID number once the tenders and amounts in the Transaction Tender List grid are defined, and the Cash Office Activity is saved.|
|Transaction Date|The date the selected Cash Office activity was performed. The system automatically assigns the time once the tenders and amounts in the Transaction Tender List grid  are defined, and the Cash Office Activity is saved.|
|From Account|The account from which money for the defined activity is transferred from.|
|To Account|The account to which money for the defined activity is transferred to.|
|Account|The account for which the defined activity is performed. The Account value is automatically populated when  button is clicked.<BR>**Note:** The Account field is displayed when Till Declaration, Bank Deposit, and Safe Declaration are selected.|
|Total|The total activity amount.|
|Reference|The activity reference for each cash office activity performed in the store. This is a free text field and can contain up to 50 characters.|
|**Transaction Tender List**|Displays the details of the tenders used in the cash office activity.|
|Tender ID|The tender used in the cash office activity.<BR>**Note:** Only the tenders defined in the Tenders module for the selected cash office activity can be selected.|
|Amount|The amount of each tender used in the cash office activity.|
|Converted Rate|The equivalent tender amount in the local currency. When entering an amount in a foreign currency, the system calculates the amount in the local currency based on the currency rates defined in Currency Exchange Rates. Once the tender amount is converted to the local currency, the system automatically populates the Converted Rate field with the converted amount.|

### Tax Rates

The Tax Rates screen displays all the tax rates defined in the Tax Rates module.

![Tax Rates Screen](/Images/BusinessPeriodsActivitiesTaxRatesScreen.png)

View the fields as follows:

|**Field**|**Description**|
|---------|----------|
|**Description**|The name of the tax rate.|
|**Method**|The method used to calculate the tax rate, e.g., Percent, Fixed.|
|**Rate**|The tax rate value.|
|**Tax Amount**|The tax amount applied in the Cash Office Activity. You can manually enter the tax amount to be applied in the Cash Office Activity based on the relevant Tax Rate.<BR>The Tax Amount can be adjusted based on the Tax Entry is Adjustable parameter in the Account Profile screen. When selected, the Tax Amount can be adjusted.<BR>If the parameter is not selected, the Tax Amount field cannot be adjusted. See also: Account Profile.<BR>On viewing the Tax Rates screen from the Activity Search screen, the Tax Amount field is read-only and cannot be changed.<BR>**Note**: Adjusting tax amounts does not flag the activity as an adjusted transaction. Searching for adjusted Cash Office Activities in the Activities Search screen does not retrieve activities in which only the tax amount was adjusted.|
|**Total**|The total tax amount applied in the Cash Office Activity.|
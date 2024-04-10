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

The Tax Rates screen displays all the tax rates defined in the Tax Rates module. See also: Tax Rates.  
During a Cash Office Activity flow for a Paid In or Paid Out, The Tax Rates screen is displayed and the user can enter a Tax Amount for each tax rate.  
The following screen shows an example of the Tax Rates screen:


![Tax Rates Screen](/Images/BusinessPeriodsActivitiesTaxRatesScreen.png)

View the fields as follows:

|**Field**|**Description**|
|---------|----------|
|**Description**|The name of the tax rate defined in the system.|
|**Method**|The method used to calculate the tax rate, e.g., Percent, Fixed.|
|**Rate**|The tax rate of the defined tax.|
|**Tax Amount**|When the Tax Entry Details field is set to By Tax Amount - indicates that the system only calculates the total Tax Amount based on the tax amount(s) entered by the user for existing Tax rates.<br>By Taxable amount – indicates that the taxable amount can be entered per existing Tax rate. Based on the taxable amount entered by the user and the tax rate, the system will calculate and display the tax and total amount per Tax Rate and the overall Total Amount after Tax.<br>The tax amount applied in the Cash Office Activity.<br>When the **Tax Entry Details** field in the Account Profiles/Tax Association is set to By Tax Amount, you can manually enter the tax amount to be applied in the Cash Office Activity based on the relevant Tax Rate. The system calculates the total Tax Amount based on the tax amount(s) entered by the user for existing Tax rates. See also: Account Profile.<br>If the **Tax Entry Details** field is set to **By Taxable Amount**, you can enter the taxable amount per Tax rate in the Net Price field, and the system calculates and displays the tax and total amount. At that point (or later when opening an existing activity) the user can correct the Tax Amount (within the specified correction range) that was calculated by the system in case of any differences in rounding done by the system and compared to the original receipt for that activity.<br><br>**Note:** On clicking the OK button in the Tax Rates screen, if no tax or net price, i.e., the taxable amount has been entered, the system prompts a configurable error message: e.g., ‘Tax does not exist for any of the tax rates’ and when clicking OK on the error message the Tax entry screen is not closed.<br>The user must enter a Tax/Net price (Taxable amount). You cannot save an activity if there is not at least one Tax/Net Price (Taxable amount) entered for one of the existing tax rates.<br><br>On viewing the **Tax Rates** screen from the **Activity Search s**creen, the **Tax Amount** field is read-only and cannot be changed.<br><br>**Note:** Adjusting tax amounts does not flag the activity as an adjusted transaction.|
|**Net Price**|The taxable amount per tax rate. (The user who enters the taxable amount, normally has the original receipt that belonged with that activity. This receipt should contain the net price next to the tax and total amounts.)<br><br>**Note:** The **Net Price** and **Total Amount** fields are only displayed if the **Tax Entry Details** field in the Account Profiles/Tax Association drawer is set to **By Taxable Amount**. See Account Profiles.<br>![Tax Rates Screen](/Images/TaxRatesNetPriceScreen.jpg)|
|**Total Amount**|The total amount (calculated total by the system, based on the taxable amount entered and the tax rate)|
|**Total**|The total tax amount applied in the Cash Office Activity.|
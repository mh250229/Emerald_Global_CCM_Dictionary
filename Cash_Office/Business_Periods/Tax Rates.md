### Tax Rates

The **Tax Rates** screen displays all the tax rates defined in the Tax Rates module. See also: [Tax Rates.](../../Financial/Tax/Tax_Rates.md)  
During a Cash Office Activity flow for a Paid In or Paid Out, the Tax Rates screen is displayed and the user can enter a Tax Amount for each tax rate.  
The following screen shows an example of the Tax Rates screen:


![Tax Rates Screen](/Images/BusinessPeriodsActivitiesTaxRatesScreen.png)

View the fields as follows:

|**Field**|**Description**|
|---------|----------|
|**Description**|The name of the tax rate defined in the system.|
|**Method**|The method used to calculate the tax rate, e.g., Percent, Fixed.|
|**Rate**|The tax rate of the defined tax.|
|**Tax Amount**|When the Tax Entry Details field is set to By Tax Amount - indicates that the system only calculates the total Tax Amount based on the tax amount(s) entered by the user for existing Tax rates.<br>By Taxable amount – indicates that the taxable amount can be entered per existing Tax rate. Based on the taxable amount entered by the user and the tax rate, the system will calculate and display the tax and total amount per Tax Rate and the overall Total Amount after Tax.<br>The tax amount applied in the Cash Office Activity.<br>When the **Tax Entry Details** field in the Account Profiles/Tax Association is set to By Tax Amount, you can manually enter the tax amount to be applied in the Cash Office Activity based on the relevant Tax Rate. The system calculates the total Tax Amount based on the tax amount(s) entered by the user for existing Tax rates. See also: [Account Profile](<../../Cash_Office/General/Account_Profiles.md>).<br>If the **Tax Entry Details** field is set to **By Taxable Amount**, you can enter the taxable amount per Tax rate in the Net Price field, and the system calculates and displays the tax and total amount. At that point (or later when opening an existing activity) the user can correct the Tax Amount (within the specified correction range) that was calculated by the system in case of any differences in rounding done by the system and compared to the original receipt for that activity.<br><br>**Note:** On clicking the OK button in the Tax Rates screen, if no tax or net price, i.e., the taxable amount has been entered, the system prompts a configurable error message: e.g., ‘Tax does not exist for any of the tax rates’ and when clicking OK on the error message the Tax entry screen is not closed.<br>The user must enter a Tax/Net price (Taxable amount). You cannot save an activity if there is not at least one Tax/Net Price (Taxable amount) entered for one of the existing tax rates.<br><br>On viewing the **Tax Rates** screen from the **Activity Search s**creen, the **Tax Amount** field is read-only and cannot be changed.<br><br>**Note:** Adjusting tax amounts does not flag the activity as an adjusted transaction.|
|**Net Price**|The taxable amount per tax rate. (The user who enters the taxable amount, normally has the original receipt that belonged with that activity. This receipt should contain the net price next to the tax and total amounts.)<br><br>**Note:** The **Net Price** and **Total Amount** fields are only displayed if the **Tax Entry Details** field in the Account Profiles/Tax Association drawer is set to **By Taxable Amount**. See [Account Profiles](<../../Cash_Office/General/Account_Profiles.md>)<br>![Tax Rates Screen](/Images/TaxRatesNetPriceScreen.jpg)|
|**Total Amount**|The total amount (calculated total by the system, based on the taxable amount entered and the tax rate)|
|**Total**|The total tax amount applied in the Cash Office Activity.|

### Entering the Taxable Amount in the Activities Screen for a new Paid Out Activity 

**Prerequisites:**

Configure Tax Rates – for example, 0%, 9%, and 21%.

The Cash Office Profile, with account A linked, is configured as an ‘Income and Expense’ type account with Source Activities set to Paid In and Target Activities set to Paid Out.

For the Income and Expense account type, the Account Profile configuration ‘Allow Tax Entry’ field is set to ‘Yes’ and ‘Tax Entry Details’ is set to ‘By Taxable Amount’.

The User is configured with Cash Office Permissions.

1. Log in to the CCM.
1. Browse to Cash Office/Business Periods/Activities and open the Activities Screen
1. Select a store and select Paid Out.
1. For the From Account and To Account fields select the Till from which you are performing the pay out and the Income and Expense account to which you are performing the payout.
1. In the Reference field enter a reference, if relevant.
1. Select Add New +.  
![Tax Rates Screen](/Images/newpaidoutscreen.png)  
1. In the Transaction List window in the line of the new Paid Out activity, select the icon next to the Tax field.  
![Transaction List window](/Images/transactionlistwindow.png)  
The Tax Rates screen is displayed, and there is an option to enter the taxable amount per tax rate. 
Enter a taxable amount for at least one tax rate. When exiting the Taxable Amount/Net Price field, or when saving the activity, the Tax and Total amounts are calculated by the system.  
If the system is configured to Allow Tax entry corrections, a correction can be made to the Tax amount that was calculated by the system in case of any difference between the tax amount calculated and the tax amount on the original receipt:
![Tax rates screen](/Images/taxratestaxratesscreen.png) 
1. Select OK to save the tax. 
![Tax rates screen](/Images/savetaxscreen.png) 
1. Enter the tender amount equal to the total amount after tax.
1. Click Save to save the activity.
![Tax rates screen](/Images/savetaxscreen2.png) 
1. Select to Print. The Activity Printout contains the Tax information per Tax rate including the Taxable amount.

If the system is configured to Allow Tax entry corrections, the user can go back to the Tax Rates screen and is allowed to edit the calculated amounts. If a threshold is defined, the user cannot exceed the threshold, if the threshold percent/amount value is exceeded, an error is prompted.
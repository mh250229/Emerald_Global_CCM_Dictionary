### Transaction List

**Transaction List** is used to view the details of the Cash Office activities performed in the selected business period. The Transaction List is displayed on selecting the Cash Office Activity in the Till Transaction Screen and clicking the blue View Transaction link.

**Reference Path:** *Cash Office/Business Periods/Till/Cashier Pending Periods/Till Transactions/Transaction List*

![Down arrow icon](/Images/transactionlistscreen2.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store in which the activity was performed.|
|**Activity Name**|The name of the cash office activity.|
|**Account**|The touchpoint account in which the activity was performed.|
|**User**|The name of user who performed the transaction.|
|**Start Business Date**|The start date of the business period in which the activity was performed.|
|**End Business Date**|The end date of the business period in which the activity was performed.|
|**Monetary Adjusted Transactions Only**|Indicates that only Cash office activities in which at least one adjustment was performed are retrieved and displayed in the Cash Office Activities Log grid.|
|**Activities**||
|Transaction Date|The date and time the Cash Office Activity was performed.|
|Id|The ID of the Cash Office Activity.|
|User|The name of the user who performed the activity.|
|Reference|The reference to the Cash Office Activity defined when performing the activity, e.g., an invoice number.<BR>The reference text can be adjusted based on the IsReferenceAdjustable parameter configuration in the ActivityReferenceConfigurationMaintenanceRequest RTI.<BR>When the parameter is set to True, the **Reference** field can be adjusted.<BR>**Note**: The **Reference** field cannot be adjusted for Cash Office Activities in settled Business Periods.|
|Activity Name|The name of the Cash Office Activity.|
|From Account|The account from which money for the defined activity is transferred.|
|To Account|The account to which money for the defined activity is transferred.|
|Total Amount|The total amount in the transactions.|
|Tax Amount|The tax amount applied in the Paid In or Paid Out Cash Office Activity.<BR>If the Tax Amount is a fixed amount, the field is read only and cannot be modified.<BR>If the Tax Amount is based on a Tax Rate, an ![Tax rate icon](/Images/taxrateicon.png) icon is displayed in the field. On clicking the icon, the Tax Rates screen is displayed showing the updated tax amount per tax rate. See also: Tax Rates<BR>**Note**: The **Tax Amount** field is only displayed for Paid In and Paid Out Cash Office Activities.|
|Over / Short|The over/short amount declared for the activity.<BR>The options are:<BR>* **Over** - The declared Tender is more than the calculated value. Over amounts are a positive number and Over is displayed next to the amount.<BR>* **Short** - The declared Tender is less than the calculated value. Short amounts are a negative number and Short is displayed next to the amount.|
|**Tenders**||
|Customize Columns|Enables you to select the columns displayed in the Tenders grid. To select the column, click ![Down arrow icon](/Images/downarrowicon.png) . A list of the available columns is displayed. Select the columns you want to display in the grid.|
|Tender ID|The ID of the tender recorded in the activity.|
|Tender Name|The name of the tender.|
|Original Amount|The amount originally paid in the transaction.|
|Original Converted Rate|The tender amount in the base currency, e.g., the currency from which you are converting.|
|Total Amount|The total tender amount for the activity.|
|Amount|The converted tender amount.|
|Converted Rate|The currency exchange rate.|
|Reason|The reason for the over/short amount, if the amount is not balanced.|
|Over / Short|The over or short amount declared for the activity.|
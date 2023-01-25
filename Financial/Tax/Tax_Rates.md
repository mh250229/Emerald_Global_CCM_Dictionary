## Tax Rates

**Tax Rates** define tax rates or codes. Often there are special tax rates on certain items to comply with government rules and regulations.

Tax rates may differ in different locations, and you can link different taxes to specific locations. Tax rates can be calculated by different methods. Emerald Global supports fixed, percent, Multi Tiered, Top Tiers, Multi Tiered Brackets, and Top Tiered Brackets and Brackets tax calculation methods.

Tiered taxes enable tax authorities to apply different tax rates to an item, according to the rates per tier.  In addition, the tax can be calculated per tier and the relevant tax bracket.

A unique tax engine calculates taxes during the transaction based on predefined configuration.

**Reference Path:** *Financial/Taxes/Tax Rates*

![Tax Rates Screen](/Images/TaxRatesScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Rate Id**|The tax rate ID.|
|**Authority**|The tax authority which determined the tax rate.|
|**Product group**|The product group the tax is applied to. Similar items which are taxed identically are grouped in a product group and the tax is applied to the group.
|**Date range**|The date range during which the tax rate is applied.|
|**Type**|The type of tax. The options are:<BR><BR>**Tax** - a tax applied by a tax authority<BR>**Item Fee** - a fee triggered by a specific item in the transaction. The fee amount is printed under the item in the receipt and displayed under the item line on the POS.<BR>**Transaction Fee** - a fee triggered by each item in the transaction. The fee amount is printed at the end of the transaction in the receipt and displayed at the end of the transaction on the POS.|
|**Location**|The store or store hierarchy in which the tax is applied.|
|**Tax Zone**|The geographical area or zone in which the tax is applied.|
|**Grid area**|
|Rate ID|The tax rate ID.|
|Description|The name of the tax rate.|
|Method|The method used to calculate the tax rate.<BR>The options are:<BR>Fixed, Multi tiered, Top tier, Proportional percentage.|
|Rate|The tax rate value.|
|Start at|The date from which the tax rate is applied.|
|End at|The date up to which the tax rate is applied.|
|Type|The Tax type, e.g., Tax, Item Fee, Transaction Fee.|
|Tax Zone|The geographical area or zone in which a tax is applied.|
|Product group|The group of products to which the tax is applied.|
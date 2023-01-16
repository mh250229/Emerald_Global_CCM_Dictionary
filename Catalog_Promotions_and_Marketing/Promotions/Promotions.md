## Promotions

**Promotions** is based on a flexible building blocks concept. The Promotion Manager’s building blocks enable you to create very simple to very complex promotions. The Promotion Manager includes a  Toolbox feature with Criteria, Reward, Financial, Controls and Restrictions, and Market Attribute options.

The toolbox options contain boxes of functions. Each box contributes to the vast array of dynamic features and functions from which you can build your promotion. On selecting a function, it is applied with a default value, making set up very easy and efficient. The concept brings a fresh approach with an unlimited range of combinations to build any promotion.

For example, a basic promotion can include one criterion and one reward, for example, Buy 1 Chocolate bar, Get 1 Free, whereas a complex promotion may include a range of criteria and even more than one reward, e.g., Buy 1 Chocolate bar, and spend a minimum of $50.00 in the ticket and Get 1 Free and Earn 500 points this visit. The options are endless.

All this functionality is made available by the Promotion Engine with its extensive capabilities in order to create promotions fully compliant with customization.

The Promotion engine enables the integral capabilities of the Promotion Manager to support the full cycle from promotion setup at the central office, store level, online distribution of promotions to all or selected stores, and executing the promotions at the time of checkout. The promotion manager also supports importing different promotions from 3rd party systems.

Part of the roadmap is to define a unique functionality where templates can be built for the different promotion types, which save setup and maintenance time. This functionality will be elaborated on in future versions.

Currently, Loyalty is integrated on a very low level, enabling the option to link promotions to segments and member accounts. In future releases, the Promotion Manager will integrate fully with the Loyalty and Promotion Engine.

Apportionment can also be defined according to the user’s requirements.

**Reference Path:** *Catalog, Promotions & Marketing/Promotions/Promotions*

![Promotions Screen](/Images/PromotionsScreen.png)

|**Field**|**Description**|
|---------|----------|
|**ID**|The Promotion ID number.|
|**Description**|The promotion name.|
|**Exact Match**|Indicates if only promotions with the exact Promotion ID or Description are included in the search results.<br>For example, if you enter 123 in the ID field, and select Exact Match, only promotion #123 is displayed in the grid. If you do not select Exact Match, any promotion with the combination of 123 in the ID number is retrieved, e.g., 123456, 484123, 512346.|
|**Start Date**|The date the promotion started running in the stores.|
|**End Date**|The date the promotion stopped running in the stores.|
|**Suspended**|Indicates that the promotion is not running in the stores. The options are:<br>**All** - includes both active and suspended promotions<br>**Suspended** - includes only suspended promotions<br>**Not Suspended** - includes only active promotions|
|**Manual**|Indicates if the promotion is a manual promotion. The options are:<br>**All** - includes both manual and automatically triggered promotions<br>**Manual** - includes only manually triggered promotions<br>**Not Manual** - includes only automatically triggered promotions|
|**Stores**|The stores in which the promotion is running.|
|**Items**|The items linked to the promotion.|
|**Touchpoint Groups**|The Touchpoint Group comprising the touchpoint on which the promotion was triggered. Multiple Touchpoint Groups can be selected.|
|**Coupon Series / Instance OR Coupon barcode**|The coupon series/instance or coupon barcode linked to the promotion.<br>To search for promotions by the coupon barcode, in the Coupon barcode field, enter the full or partial barcode of the coupon.<br>If both a Coupon Series and a Coupon Barcode are selected, promotions which meet either of the criteria are retrieved.<br>When searching for promotions by the Coupon Instance, both the Coupon Series and Offer Code are required. If only the Offer Code is sent, an error message is returned.|
|**Linkage Type**|The coupon type linked to the promotion. The options are:<br>**All** - Retrieve both issuing and redemption promotions.<br>**Issuing** - Retrieve promotions in which the coupon is issued as a reward. Once the promotion is triggered, the customer receives a coupon which can be redeemed later.<br>**Redemption** - Retrieve promotions in which the coupon triggers the promotion and the customer receives the coupon reward. Once the coupon is scanned and the promotion is triggered, the customer receives the reward.|
|**Promotions**|The promotions that meet the selected search criteria are displayed in the grid. If no search criteria are entered, all the promotions are retrieved.|
|Id|The Promotion ID number.|
|Description|The promotion name.|
|Suspended|The promotion is temporarily suspended from running during the defined promotion date range. The options are:<br>**No** - The promotion is active.<br>**Yes** - The promotion is suspended.|
|Start Date|The date and time from which the promotion is active in the store.|
|**End Date**|The date and time up to which the promotion is active in the store.|

**Reference Path:** *Catalog, Promotions & Marketing/Promotions/Promotions/Add New*

![Promotions Form](/Images/PromotionsForm.png)

|**Field**|**Description**|
|---------|----------|
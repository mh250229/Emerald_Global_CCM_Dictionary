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
|ID|The unique promotion ID number. The promotion ID number is assigned when a promotion is created by one of the following methods:<br><br>Imported from an external system.<br>Configured manually and the ID is assigned by the user.<br>Configured manually and the ID is generated automatically. If the server receives a promotion without an ID, a default ID is generated.<br><br>The ID, Description, and Start fields are mandatory.|
|Short Description|The promotion description displayed at the touchpoint. If a long description is not defined, the short description is printed on the receipt.|
|Long Description|The promotion description printed on the receipt. 
The Long Description is not mandatory. If the Long Description is not defined, the Short Description is used instead.|
|Start|The date and time on which the promotion starts. You can assign the same promotion to different stores in different periods of time.|
|End|The date and time on which the promotion ends. The End date is not mandatory. If an End date is not defined, the promotion runs indefinitely.|
|Suspended|The promotion is not running in the stores. If set to Yes, the promotion is stopped from running in the store, even if the start and end dates are active.<br>This option is used to temporarily suspend a promotion from running during a specific period of its life cycle.|
|Select Drawer|Contains the conditions and criteria to define promotions. Each drawer contains specific parameters.<br>The following drawers are available:<br>**Criteria** – to define the criteria that triggers the promotion. You can include a variety of criteria enhancing your promotion to meet complex business requirements.<br>**Reward** – to define the promotion reward. A wide range of reward types can be defined, starting from a simple free item, amount or percent off, and extended to, vouchers, coupons, targeted messages, customer accounts (points), and more.<br>**Financial** – to define the financial limitations applied to a promotion, such as discount allocation and funding.<br>**Controls & Restrictions** – to define the promotion timing and conflict policies applied to a promotion.<br>**Marketing Attributes** – to define the promotion information displayed on a marketing channel to advertise the promotion and enable the customer to easily understand the promotion offer.|
|Trigger Promotion by Item Sale Time|This determines whether the promotion is triggered according to the time the transaction started or the time the item was added to the promotion.|

### Criteria

The **Criteria** option defines the conditions and the trigger values which specifies the promotion requirements to trigger the promotion reward.

![Criteria Screen](/Images/CriteriaScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Basket**|Defines the items in the promotion, which when purchased trigger the promotion.|
|Basket Name|The name of the Basket. The Basket comprises the items on promotion. You can select the items in the basket and then apply a range of conditions to specify that if the conditions defined in the basket are met, the promotion is triggered.<br>You can define more than one basket to apply multi conditions on different baskets. Each basket must have a name to distinguish between conditions. You can manually enter alphanumeric characters in the Basket name to provide meaningful names to enable you to easily track them. The name entered in the Basket Name field is displayed in red font in Basket section header.|
|Purchase Requirements|The conditions and values that must be met to trigger the promotion.|
|Type|The threshold option by which items must be purchased to trigger the promotion. This field is mandatory.<br>The options are:<br>**Units** - The item must be purchased in single units. E.g., Buy 4 Cokes Get Reward<br>**Spend** - The promotion is triggered by the amount spent on items or in the ticket. For example, spend $10.00 on the specified items. E.g., Spend $10.00 on Coke Get Reward.<br>Spend disables the New Price, Free Item, Amount Off (per Item), and Percent Off (per item) reward types. If selected, an error message is displayed when the promotion is saved.<br>**UOM Quantity** The items must be purchased by a unit of measure, e.g., kilogram, grams, liters, pounds.<br>The UOM conditions have three digits after the decimal point. For example, if you enter, 14.588888, the system saves it as 14.589. If you enter 32.1, the system saves it as 32.100.<br>You can limit the UOM quantity rewarded in a promotion. For example, Buy 1 kg Get $1.00 Off, you can limit the reward to up to 3 kg. If the customer purchases 4 kg, they only receive a $3.00 reward.<br>**Spend Any Value** - The promotion is triggered when any amount is spent. No threshold is defined, for example, Spend any amount on Dairy products, Get 10% Off.<br>The promotion reward for the Spend Any Value type is usually Percent Off as the amount which triggers the promotion is not known and a fixed reward, e.g., Amount Off can be more than the item price. If the reward type is Amount Off, and the reward amount is more than the item price then a partial reward is given.<br>New Price or Free Item rewards can only be selected if another condition is defined in the promotion. For example, Spend Any Value on Dairy products and Buy 2 Milk Get One Free, the free item reward is issued only on the Milk.<br>**Any Quantity UOM** - to set a UOM promotion for any quantity bought, without specifying a threshold.  For example, Get the New Price of $4.00 per kilo for any quantity purchased. The promotion reward applies to the entire UOM quantity bought without a threshold. If the customer purchased 0.05 kg, they pay $1.00.<br>Although the promotion redemption is always 1, you can limit the UOM quantity rewarded in a ticket.<br>When selected, the Threshold Value and Reward Calculation on Threshold Value fields are not enabled.|
|Threshold Value|The threshold value of the threshold option selected in the Type field. For example<br>In the promotion Buy 4 Cokes Get a Reward, select **Unit** and in **Threshold Value** enter 4 to specify the number of items that must be purchased to trigger the promotion.<br>In the promotion Spend $50.00 get 10% Off, select **Spend**, and in **Threshold Value** enter 50 to specify the amount that must be spent to trigger the promotion.<br>The Threshold Value field is disabled when **Type** is set to **Spend Any Value**.|
|Customer Must Buy|The items the threshold option selected in the Type field applies to. The options include:<br>**Any Item** – indicates that the customer can purchase any of the items in the list of conditions, as long as the value is met (displayed by default).<br>**Same Items** – indicates that the customer must purchase the specified number of the same item within the list of conditions.<br>For example: Buy four identical items and receive a discount. In this example, the Customer Must Buy value is Same Items and the Threshold Value is 4.<br>Sale 1 - The customer buys 2 identical items. The promotion is not triggered.<br>Sale 2 - The customer buys 4 identical items. The promotion is triggered, and the customer receives a discount.<br>**Different Items** – indicates that the customer must purchase the specified number of items, but each item must be different.|
|
## Product View

**Product View** is used to search for items, and view item details, such as the price, additional codes, etc. You can search for an item in a specific store or item hierarchy.

**Reference Path:** *Catalog, Promotions & Marketing/Store Catalog/ Product View*

 ![Product View Screen](/Images/ProductViewScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Store**|The store in which the item is sold.|
|**Item Code**|The item code number.|
|**Exact Match**|Indicates that only items with the exact item code entered in the Code field are included in the search results. If not selected, all items with the combination of the specified item code are retrieved.<BR>For example, if you enter 123 in the Item Code field, and select Exact Match, only item #123 is displayed in the grid. If you do not select Exact Match, any item with the combination of 123 in the Item number is retrieved, e.g., 123456, 484123, 512346.|
|**Item Description**|The item description.|
|**Merchandise Hierarchy**|The item hierarchy.|
|**Weak Search Criteria**| Indicates that the search results are limited to the first 300 items that meet the Search criteria, and that additional search criteria should be added to narrow down the results.|
|**Items**||
|Status|The item status. The options are:<BR>![Green Check Mark Icon](/Images/GreenCheckMarkIcon.png) indicates the item can be sold in the selected store.<BR>![None Icon](/Images/NoneIcon.png) indicates that the item is not included in the store variety for the selected store.<BR>![Lock Icon](/Images/lockicon.png) indicates that the item is locked for sale in the selected store.|
|Code|The item code number.|
|Description|The item description.|
|Merchandise Hierarchy|The item hierarchy the item is linked to.|
|Current Price|The item retail price.|

**Reference Path:** *Catalog, Promotions & Marketing/Store Catalog/Product View/Edit*

![Product View Form](/Images/ProductViewForm.png)

|**Field**|**Description**|
|---------|----------|
|**Item Code**|The item code number.|
|**In Variety**|Indicates that the item in included in the store variety.|
|**Short Description**|The item description that is displayed on the POS and on the customer receipt.|
|**Detailed Description**|The detailed description added to menu items which is displayed at the Kiosk.|
|**Additional Codes**|The Additional sellable product code used when selling the product at a touchpoint. Additional codes can be internal or external and must be unique. Items are sold at the POS terminal via the Additional (sellable) code. A product can have more than one additional codes of different types, for example, EAN, SKU, however, each type must have a unique number.<BR>The Additional Code field is not mandatory, however, you must define an additional code in order to sell the product at the touchpoint.|
|**Current Price Plans**|The item retail price per unit the item is sold by|
|**Taxes**|The tax rates applied to the item.|
|**Eligibilities**|The item/tender restrictions applied to the product, e.g. SNAP, and so on.|
|**Online Item External ID**|The External ID of the online item, if defined. The External ID is unique for each Online Item.<BR>If the Online Item does not have an External ID or the item is not an Online Item, the field is blank.
|**Merchandise Hierarchy**|The position (node) of the product in the Merchandise Hierarchy., e.g., Pizza is linked to the Dairy node in the hierarchy|
|**Item Group**||
|Deposit|The deposit amount linked to the item, for example a bottle of Coke has a $0.50 bottle deposit fee.<BR>**Note:** If the Deposit, Tare, Warranty, or Tags fields are not relevant for the selected item, None is displayed in the fields.|
|Tare|The weight of the empty package/container in which the product is sold.|
|Warranty|The warranty linked to item, for example, a T.V. is sold with a year warranty.
|Tags|Displays the tags added to the product. Tags are keywords assigned to a product to describe a specific product property, and are used to categorize products by properties, e.g., Kosher, Gluten Free, No Lactose, etc.<BR>Multiple tags can be added to a product.|
|**Sales Restrictions**|Defines sales restrictions are applied when setting up a product.|
|Locked for Sale|Indicates if the item cannot be sold or not.
|Price Entry Required|Indicates that item price must be manually entered.
|Price Verify|Indicates if the item price can be manually verified at the POS.|
|Inhibit Quantity Keyed|Indicates if the item quantity sold cannot be keyed in manually at the POS.|
|**Calories Information**||
|Unit of Measurement|The UOM used to calculate the item calories. Each item can have only one UOM. UOMs can be per weight, e.g., gr, kg, lb, or each. Each refers to the relevant serving size, e.g., slice, cup, spoon.|
|Quantity|The quantity of the item which reflects the calculated calories value.|
|Basic Calories Value|The number of calories, per the quantity and the UOM.|
|Current Display|The calorie value according to Display Type option selected in Product Maintenance.<BR>The Display Type options are:<BR>**Single** – If selected, the Current Display field displays the Basic Calories Value for the item, e.g., 520. This is the default.<BR>**Two** – If selected, the Current Display field displays the minimum and maximum number of calories calculated for the item, e.g., 420/700.<BR>**Range** – If selected, the Current Display field displays the calorie range for the item, e.g., 420 – 700.<BR>**Note:** Modifiers are always presented in the Single Value format.|
## Product Maintenance

**Product Maintenance** is used to add a product to the Store Catalog or modify the product details at the HQ level.

In addition, you can define restrictions, prices and the stores in which the product can be sold.

**Reference Path:** *Catalog, Promotions & Marketing/Store Catalog/Product Maintenance*

![Product Maintenance Screen](/Images/ProductMaintenanceScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Item Code**|The ID of the product you want to view.|

### General Tab

The General tab displays and modifies product details, such as the item description and sellable codes. The product details are updated in the catalog at HQ level.

**Note:** Only users assigned to Roles with the relevant permissions can update product details.

![General Tab](/Images/GeneralTab.png)

|**Field**|**Description**|
|---------|----------|
|**Descriptions**||
|Short Description|The product description displayed at the POS terminal.|
|Description|The long description of the product as defined in the database.|
|Detailed Description|A detailed description of menu items displayed at the Kiosk.<BR>The description can include, for example, a list of ingredients for the item or preparation instruction, such as 'Tender grilled chicken with lettuce, tomato & onion on white bread' can be added for the ‘Grilled Chicken Sandwich’ menu item.<BR>At the kiosk the menu item is displayed with the detailed description under the item.<BR>The field is optional and can include up to 255 characters.
|**Additional Codes**|The Additional sellable product codes that are used when selling the product at a touchpoint. Additional codes can be internal or external and must be unique. Items are sold at the POS terminal via the Additional (sellable) code. A product can have more than one additional codes of different types, for example, EAN, SKU, however, each type must have a unique number.<BR>The Additional Code field is not mandatory, however, you must define an additional code in order to sell the product at the touchpoint.|
|**Merchandise Hierarchy**|The node the selected product is linked to in the Merchandise hierarchy. The Merchandise Hierarchy categorizes all the items in the Store catalog in a hierarchy based on the department, sub department and category of each product.|
|**Calories Information**||
|Unit Of Measurement|The UOM used to calculate the item calories. Each item can have only one UOM. UOMs can be per weight, e.g., gr, kg, lb, or each. Each refers to the relevant serving size, e.g., slice, cup, spoon.|
|Quantity|The quantity of the item which reflect the calculated calories value.|
|Basic Calories Value|The number of calories, per the quantity and the UOM.|
|Display type|Specifies how the calorie information is displayed in the Current Display field in the Product View screen.<BR>The options are:<BR>* **Single** – indicates that the Basic Calories Value for the item is displayed, e.g., 520. This is the default.<BR>* **Two** - indicates that the minimum and maximum number of calories are displayed, 420/700. Up to 11 characters are supported.<BR>* **Range** – indicates that the calorie range is displayed, e.g., 420 – 700. Up to 11 characters are supported.|
|Min Calories Value (if any)|The minimum number of calories is the sum of all the required item modifiers set to their Min portion.|
|Max Calories Value (if any)|The maximum number of calories is the sum of all the item modifiers set to the Max portion.|

### Restrictions Tab

The **Restrictions tab** is used to apply restrictions on selected products.

Restrictions can be defined at HQ level and inherited by the Business Units or defined for a specific Business Unit. A restriction applied to a specific Business Unit overrides the same restriction applied at HQ level.

When a restriction applied to a specific Business Unit is deleted, and the same restriction exists for the selected product at the root level, the Business Unit automatically inherits the restriction.

Once a restriction is deleted at all levels, the product is no longer restricted. Outdated (expired) restrictions are not displayed.  

**Note:** Only users assigned to Roles with the relevant permissions can apply restrictions.

![Restrictions Tab](/Images/RestrictionsTab.png)

|**Field**|**Description**|
|---------|----------|
|**Locations**|The specific node in the hierarchy the restriction is applied to.<BR>Once a level is selected, restrictions defined for the product at the selected level are displayed. Root level restrictions apply to all business units/stores.<BR>**Note:** Only stores which the user has permissions to access are displayed.|
|**Restrictions**|The restrictions you want to apply to the selected product.|
|Restriction Type|The restriction type you want to apply to the selected product. The options are:<BR>* **Locked For Sale** - The product is prohibited for sale.<BR>* **Manual Quantity** – specifies that the product quantity purchased must be manually entered.<BR>* **Price Entry Required** - specifies that the price of the product is manually entered<BR>* **Price Verify Required** - specifies that the price must be approved before the product is sold.<BR>* **Prohibited Keyed Quantity** - specifies that the quantity purchased cannot be manually entered.|
|Location|The level/location in the hierarchy tree to which the restriction is applied. Locations of inherited restrictions can be overridden.<BR>For example, you define a Price Verify Required restriction for a product at the Root level and specify that in a specific store the restriction is not applied by localizing the restriction and changing the details. Inherited restrictions cannot be deleted. If the overridden restriction is deleted, the restriction on the parent is re inherited.|
|Starting Date/Time|The date and time from which the restriction is applied. The starting date and time are required only for Locked For Sale restrictions.  The field is not enabled when another restriction is defined.|
|Reason|The reasons displayed at the POS when a product with a Locked For Sale  restriction is scanned. On scanning the product a list of the selected reasons is displayed and the cashier then selects the relevant reason.<BR>Reason Codes are required only for Locked For Sale restrictions. The field is not enabled when another restriction is selected.
|Enabled|Indicates that the restriction is applied to the specified location.|

### Store Range Tab

The Store Range tab is used to view the store in which the product is sold. You can define a single store or a range of stores.

Once defined, you can filter products by the store range. Only selecting a business unit from the store hierarchy, the products linked to the business unit are displayed in the Store Range grid, and are sorted according to the Effective Date, starting with the most recent effective date.

A Store Range can only be deleted if the product is linked to the actual business unit. For example, you cannot delete a Store range record at the root level ion the store hierarchy if the location is set to a lower level in the hierarchy such as South or Brooklyn.  

Inherited store ranges for a specific product can only be modified for future effective dates.

**Note:** Only users assigned to Roles with the relevant permissions can assign store ranges.

![Store Range Tab](/Images/StoreRangeTab.png)

|**Field**|**Description**|
|---------|----------|
|**Locations**|The store hierarchy from which you can select a business unit and view the products linked to the selected store.|
|**Store Range**||
|Location|The business selected in the Store Hierarchy in the Locations section.<BR>**Note:** A location can be deleted only if the Effective Date is in the future.|
|Effective Date|The date from which the product can be sold in the selected business unit. The Effective Date is based on the store time.|
|Include/Exclude|Indicates if the selected item can be sold in the selected location. If No, then the item cannot be sold in the selected location and is not displayed in the menus.<BR>If an item modifier is excluded from the store, it is not displayed in the item modifier options in the group linked to the main item.<BR>For example, on ordering a sandwich on the Kiosk or QSR touchpoints, the option to add sauce is available. If the ketchup is not in the store variety, the sauce options will not include ketchup. If ketchup is the only sauce option, then no sauce options are displayed.<BR>If an item modifier excluded from the store, and the main item cannot be sold without the modifier. the main item is marked as not for sale.<BR>For example, Tomato is not in the store variety and is a mandatory ingredient of the BLT sandwich. The BLT sandwich is marked as not for sale, and is not displayed in the menu options at the Kiosk or QSR touchpoints.|

### Price Tab

The **Price tab** is used to define prices for a selected item in a specific business unit, or at the HQ level. Only users assigned to Roles with the relevant permissions can define prices.

![Price Tab](/Images/PriceTab.png)

|**Field**|**Description**|
|---------|----------|
|**Locations**|The store hierarchy from which you can select a business unit and view the products linked to the selected store. Once a level is selected, the item price defined for the product at the selected level is displayed.<BR>Prices applied at the Root level are applied to all the Business Units/Stores.<BR>**Note:** Only stores to which the user has access permission are displayed.|
|**Prices**|The prices that apply to the selected product.|
|Location|The location where the price applies. If an inherited price exists for the select product, you must localize it to be able to assign the new price locally. Users can delete a price. If a local price is deleted, and an inherited price exists, it is automatically applied.<BR>The location and hierarchy (selected in the Locations panel) are the same. The user must first select the Business Unit from the tree, which creates a Price Entry that can be modified. The Price Entry has the Location as an attribute.|
|Unit of Measure|The unit by which the item is sold, for example, Kg. Only one UOM can be defined for the product in each Business Unit.|
|Pricing qty|The number of units included in the price. For example, three packets of Candy are sold for $9.00. In this example, the Pricing Quantity is 3.<BR>The pricing quantity must be a whole number greater than 0 and cannot be a decimal. If a value is not entered, then the product price is for one unit of the selected Unit of Measure.|
|Price|The retail item price defined for the selected Business Unit. Prices can be deleted but products without a price cannot be sold at a touchpoint.|
|Currency|The currency in which the item price is defined.|
|Last Updated – Date/Time|The date and time that the price was last updated.|
|Start Date/Time|The date and time from which the price is applied. Only future start dates can be modified. Start dates with past or current dates cannot be modified.|
|End Date/Time|The date and time up to which the price is applied. The End Date can be modified for prices with start date in the past or present.|
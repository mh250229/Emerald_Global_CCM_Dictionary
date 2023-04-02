## Local Price

**Local Price** is used to update prices in the stores. Prices can be entered for a specific store and applied for a limited time period. The system tracks who made the change and when. Existing prices are not overwritten (even if they are not used) and no access is given to other stores.

When an item is scanned at the POS, the system will display the store’s most recent active price for the item.

**Note:** Local price changes can also be made in the Product Maintenance module in the Price screen, however, the user who made the change is not recorded, and there is no way to track the user who made the change.

**Reference Path:** *Catalog, Promotions & Marketing/Store Catalog/Local Price*

![Local Price Screen](/Images/LocalPriceScreen.png)

|**Field**|**Description**|
|---------|----------|
|Store|The name of the store in which the user is updating an item’s price.|
|Product Code|The item for which the price is being updated.|
|**Price Details section**|| 
|New Price|The new price of the item. This field is mandatory and can be edited.|
|Start Date|The date from which the new price is applied to the item. By default, the current date/time is applied. The date can only be changed to a future date.|
|Start Time|The time from which the new price is applied to the item.|
|End Date|The date up to which the new price is applied to the item. By default, the current date/time is applied. The date can only be changed to a future date.|
|End Time|The time up to which the new price is applied to the item.|
|Reason|The reason the item price was changed.|
|Original Price|The item’s last effective price that is not a result of local price change.|
|Current Effective Price|The current price of the item. This price cannot be changed.
|Quantity|The quantity to which the price applies. This field can only be updated if no previous price existed.|
|Unit Of Measure|The Unit of measurement to which the price applies. This field can only be updated if no previous price existed.|
|Currency|The store currency. This field cannot be updated.|
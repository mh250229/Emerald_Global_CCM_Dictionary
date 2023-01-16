## Promotion Groups

**Promotion Groups** are used to allow users to manually intervene in the prioritization of promotions.

Promotions are assigned to a Promotion Group, which is then prioritized. The priority determines the order that promotion groups are executed.

For example, the promotions in a Promotion Group assigned to Priority 1 are executed before the promotions in a Promotion Group assigned to Priority 2, and so on.

**Scenario:**

* Group 1 with Priority ID 2
* Group 2 with Priority ID 3
* Group 3 with Priority ID 1

The promotions in Group 3 run first, then Group 1 and lastly Group 2.  
Promotion Groups are also assigned to a promotion strategy. The following three promotion strategies enable the retailer to handle promotions:

* **None** - Multiple discounts are allowed, promotions are executed according to their reward type as defined in the ‘Priority Tree’ and calculated on the net price of the items.
* **Conflict** - The promotions in the Promotion Group ID are in conflict, i.e., an item can be applied to only one promotion from this group, the one that gives the best reward to the customer. 
* **Best Deal** - Rewards the customer with the most lucrative deal out of all the promotions in the group, regardless of the item

Any promotion that is not assigned to a Promotion Group is automatically assigned to the default Group 0. Group 0 must be created during the initial setup, and is assigned priority 0. The None strategy is always applied by default to Promotion Group 0.

When Group 0 exists, all new promotions created are always assigned to Group 0, up until the promotion is officially assigned to a Promotion Group. If Group 0 does not exist, all promotions not associated to a group will run before any other promotion according to the Default Priority Order. If at least one group is defined and there are promotions which are not related to any group, Group ID 0 is not automatically created automatically, and must be configured.

If you want to run a Promotion Group before the promotions in Group 0, you must assign a priority <0 to the group, for example, assign priority -1 to the Promotion Group.

**Subgroups**

A Promotion Group can include subgroups. On linking a Promotion Group to a parent group, the Promotion Group becomes a subgroup within the main Promotion Group enabling you to create a Promotion Group hierarchy.

Both parent groups and subgroups are assigned a Priority. While subgroups can be assigned to all the strategy options (Conflict/Best Deal/None), a parent group can only be assigned to the None strategy. Promotions in the parent group always run before the promotions in the linked subgroups.

**Reference Path:** *Catalog, Promotions & Marketing/Promotions/Promotion Groups*

![Promotion Groups Screen](/Images/PromotionGroupsScreen.png)

|**Field**|**Description**|
|---------|----------|
|ID|The promotion group ID.|
|Description|The name or description of the promotion group.|
|Priority|The order in which the promotion groups are executed. For example, a Promotion Group assigned to Priority 1 are executed before a Promotion Group assigned to Priority 2, and so on.|
|Strategy|The method by which the system handles promotion execution within the Promotion Group. All Promotion Groups are assigned to a strategy and then are prioritized according to the Priority ID.<BR>**None** - The system can trigger all promotions in which all the promotion conditions are met in this group. The promotions are executed according to their reward type as defined in the ‘Default Priority Order’ and calculated on the net price of the items. The default Priority Order is the best for the retailer since there are multiple promotions. This is the default value.<br>For example, ‘Buy coke ($3.00) get $1 off’ and ‘Buy coke ($3.00) get 10% off’ – when these promotions are in one group defined with the ‘None’ strategy, both promotions are triggered. According to the Default Priority Order, amount off promotions should run before percent off promotions, therefore, in this example, first $1.00 off will be reduced from the price of coke, reducing the net price to $2.00, and then 10% off, reducing the net price to $1.80. The Default Priority Order is set to try giving the customer the minimal discount, i.e., ‘Best for Retailer’, since the customer is already getting multiple discounts on the same items.<BR>**Best Deal** - The promotion with the best offer, i.e., the promotion that gives the highest reward to the customer is triggered.<BR>For example, ‘Buy a coke for $2.50 Get 10% Off and ‘Buy a Sprite ($2.50) get $0.10 off’ ¾ when these promotions are in one group defined with the ‘Conflict’ strategy, only one promotion will trigger after scanning the coke – the best one for the customer. In this example, the ‘Buy a coke for $2.50 Get 10% Off promotion is triggered.<BR>**Conflict** - The promotions in the group are in conflict, i.e., an item can be applied to only one promotion from this group. The customer is rewarded with the promotion that gives the best reward to the customer.<br>For example:<br>Promotion 1: Buy Oreo Cookies ($3.00) and get 10% off.<br>Promotion 2: Buy Oreo Cookies ($3.00) and get $0.50 off.<br>Promotion 2 will trigger (best monetary reward for customer).<br>For example, ‘Buy a coke ($3.00) get 10% Off’ and ‘Buy a Coke ($3.00) get $0.50 off’. When these promotions are in one group defined with the ‘Best Deal’ strategy, after scanning the coke, only one promotion will trigger i.e, the best one for the customer. In this example, the ‘Buy a Coke ($3.00) get $0.50 off’ promotion is triggered.<BR>**Note:** More than one promotion can be triggered in that group, for different items.<BR>***Partial Reward Conflict** - When promotions are in conflict, items can trigger more than one promotion but only rewarded in one promotion.<br>For example:<br>Buy 6 bottles of wine and get $1.00 off each bottle.<br>Buy 4 bottles of wine and get $2 off each bottle.<br>When a customer buys six bottles of wine, both promotions are triggered, however, the customer does not receive double discounts. The customer is rewarded with $2.00 off four bottles of wine, and $1.00 off the remaining two bottles of wine.<br>This provides an incentive to the customer to buy 6 bottles of wine and not just four bottles.|
|Parent Group|A Promotion Group can include subgroups. On linking a Promotion Group to a parent group, the Promotion Group becomes a subgroup within the main Promotion Group enabling you to create a Promotion Group hierarchy.<BR>Both parent groups and subgroups are assigned a Priority. While subgroups can be assigned to all the strategy options (Conflict/Best Deal/None), a parent group can only be assigned to the None strategy. Promotions in the parent group always run before the promotions in the linked subgroups.|
|

If the Edit option is selected in the grid, A Linked Promotions grid is shown below the Promotion Group.

**Reference Path:** *Catalog, Promotions & Marketing/Promotions/Promotion Groups/Add New*

![Promotion Group Form](/Images/PromotionGroupForm.png)

|**Field**|**Description**|
|---------|----------|
|ID|The promotion group ID.|
|Description|The name or description of the promotion group.|
|Priority|Indicates the priority in which Promotion Group’s promotions are run first (mandatory). It is not recommended to define groups with the same priority, however, if this happens, the execution order between the groups is according to the group ID. For example, if two groups are defined with priority ID 5, one with group ID 10 and the other with group ID 20, both will trigger after groups with priority 1-4, first the promotions within group ID 10 will trigger and then the promotions within group ID 20.|
|Strategy|The method by which the system handles promotion execution within the Promotion Group. All Promotion Groups are assigned to a strategy and then are prioritized according to the Priority ID.<br>**None** - The system can trigger all promotions in which all the promotion conditions are met in this group. The promotions are executed according to their reward type as defined in the ‘Default Priority Order’ and calculated on the net price of the items. The default Priority Order is the best for the retailer since there are multiple promotions. This is the default value.<BR>For example, ‘Buy coke ($3.00) get $1 off’ and ‘Buy coke ($3.00) get 10% off’ – when these promotions are in one group defined with the ‘None’ strategy, both promotions are triggered. According to the Default Priority Order, amount off promotions should run before percent off promotions, therefore, in this example, first $1.00 off will be reduced from the price of coke, reducing the net price to $2.00, and then 10% off, reducing the net price to $1.80. The Default Priority Order is set to try giving the customer the minimal discount, i.e., ‘Best for Retailer’, since the customer is already getting multiple discounts on the same items.<BR>**Best Deal** - The promotion with the best offer, i.e., the promotion that gives the highest reward to the customer is triggered.<BR>For example, ‘Buy a coke for $2.50 Get 10% Off and ‘Buy a Sprite ($2.50) get $0.10 off’ ¾ when these promotions are in one group defined with the ‘Conflict’ strategy, only one promotion will trigger after scanning the coke – the best one for the customer. In this example, the ‘Buy a coke for $2.50 Get 10% Off promotion is triggered.<br>**Conflict** - The promotions in the group are in conflict, i.e., an item can be applied to only one promotion from this group. The customer is rewarded with the promotion that gives the best reward to the customer.<br>For example:<br>Promotion 1 - Buy Oreo Cookies ($3.00) and get 10% off.<br>Promotion 2 - Buy Oreo Cookies ($3.00) and get $0.50 off.<br>Promotion 2 will trigger (best monetary reward for customer).<br>For example, ‘Buy a coke ($3.00) get 10% Off’ and ‘Buy a Coke ($3.00) get $0.50 off’. When these promotions are in one group defined with the ‘Best Deal’ strategy, after scanning the coke, only one promotion will trigger i.e, the best one for the customer. In this example, the ‘Buy a Coke ($3.00) get $0.50 off’ promotion is triggered.<br>**Note:** More than one promotion can be triggered in that group, for different items.<BR>**Partial Reward Conflict** - When promotions are in conflict, items can trigger more than one promotion but only rewarded in one promotion.<br>For example:<br>Buy 6 bottles of wine and get $1.00 off each bottle.<br>Buy 4 bottles of wine and get $2 off each bottle.<br>When a customer buys six bottles of wine, both promotions are triggered, however, the customer does not receive double discounts. The customer is rewarded with $2.00 off four bottles of wine, and $1.00 off the remaining two bottles of wine.<br>This provides an incentive to the customer to buy 6 bottles of wine and not just four bottles.|
|Parent Group|The Parent group of the Promotion Group. A Promotion Group can include subgroups. On linking a Promotion Group to a parent group, the Promotion Group becomes a subgroup within the main Promotion Group enabling you to create a Promotion Group hierarchy.<br>Both parent groups and subgroups are assigned a Priority. While subgroups can be assigned to all the strategy options (Conflict/Best Deal/None), a parent group can only be assigned to the None strategy. Promotions in the parent group always run before the promotions in the linked subgroups.|
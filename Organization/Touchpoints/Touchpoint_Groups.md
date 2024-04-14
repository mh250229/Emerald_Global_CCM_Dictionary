## Touchpoint Groups

**Touchpoint Groups** are used to group similar type touchpoints into groups. A touchpoint can be any client, e.g., a POS terminal, self-checkout. Venues are also defined as Touchpoint Groups. A venue is an area in the store that sells the same food type and refers to a group of touchpoints that sell the same food type, such as Italian, BBQ or Mexican.

Venues are implemented as Touchpoint Groups within a business unit.

For example:

* Set up the Main Touchpoint Group to include all the POS terminal #’s 1-4
* Set up the Express Touchpoint Group to include all the terminal #’s 5-10
* Set up the Self Checkouts Touchpoint group to include all the self-checkouts
* Set up the Italian Venue Touchpoint Group to include all the QSR terminals that sell Italian Food

When the touchpoints are defined, you link them to a touchpoint group. Every touchpoint must be connected to a certain touchpoint group in the store.

The hierarchy is defined at the chain level for all the stores. Each level can be referred to as a touchpoint group, also known as a ‘Checkout’. Each group of touchpoints can be defined to work differently.

**Reference Path:** *Organization/Touchpoints/Touchpoint Groups*

![Touchpoint Groups Screen](/Images/TouchpointGroupsScreen.png)

|**Field**|**Description**|
|---------|----------|
|Group Name|To filter for Touchpoint Groups by the name of the touchpoint group.|
|Business Unit|To filter for Touchpoint Groups by the Business Units in which touchpoint groups are assigned.|
|Group Type|To filter for Touchpoint Groups by the Touchpoint Group type.|
|**Touchpoint Groups**|
|Group Code|The touchpoint group ID number.|
|Group Name|The name of each touchpoint group created in the system, e.g., Main POS Terminals.<BR>**Note:** A Venue is an area in the store that sells the same food type. The term refers to a group of QSR touchpoints that sell the same food type.  E.g. Italian, BBQ or Mexican. Venues are implemented as Touchpoint Groups within a Business Unit.|
|Group Type|The Touchpoint Group type, either Primary or Secondary, assigned to the Touchpoint Group.<BR>All Touchpoints must be assigned to a Primary Touchpoint Group. Some touchpoints may require specific configuration are also linked to a Secondary Touchpoint Group in addition to the Primary Touchpoint Group.<BR>For example, all POS touchpoints may be assigned to the same Primary Touchpoint Group. However, some of the POS touchpoints may require different PLU menus. Retailers can assign those touchpoints to a Secondary Touchpoint Group and apply the PLU Menu configuration to the Secondary Touchpoint Group only.|
|Tags|Used to apply a tag to the Touchpoint Group. Currently, only the Venue and CTM options are supported.<BR>The options are:<BR><BR>**Venue** –The format by which the retailer can distinguish between the type of menus they are offering. For example, a retailer who is running a food court and is offering a choice between BBQ, Italian, and Sushi menus, can maintain a venue for each menu option.<BR>Once a touchpoint group is tagged as a Venue, Tabs functionality can be enabled on the touchpoint. A Tab is an open order of items to be paid for by the customer.<BR>Tabs are enabled by running the TabsConfigurationMaintenance RTI.<BR>**Note**: On setting up a QSR POS touchpoint, the retailer should only link one touchpoint to a touchpoint group tagged as a venue.<BR><br>If the Venue tag is removed from a Touchpoint Group, the system prompts the following Remove Venue Warning message:<BR>Pay attention, changes in Tag Venue may cause changes in POS behavior. Are you sure you want to continue?<BR>If you select OK, the Touchpoint group is no longer tagged as a Venue and any Tabs that were created on the touchpoint associated to the specific Touchpoint Group are no longer retrieved.<BR>**CTM** - When retailer's use a Cash Management Application ,e.g., CTM. a CTM device is installed on the store’s POS terminals. The CTM provides automated cash tendering at assisted lanes. During a transaction, notes and coins are inserted into the recycler device and change is distributed from the recycler units.<BR>All touchpoints connected to a CTM device should be configured as part of a secondary touchpoint group and tagged with the CTM Tag. This enables retailers to associate the CTM Default Cashier Account profile to the touchpoint group.|
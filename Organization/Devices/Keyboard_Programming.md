## Keyboard Programming

**Keyboard Programming** defines and customizes the keyboards of the non-touch POS terminals.

You may have different types of keyboard settings according to the different hardware manufacturers.

Keyboard Programming defines the function for each hard key. You can set up different keyboards for specific stores, or touchpoint groups and a keyboard can be assigned to multiple locations.

On a non-touch POS terminal, you must assign the function performed when selecting a key to the actual key. For example, after a cashier has scanned all the customer's items, the cashier needs to select an Enter button to move to tender mode, where payment is accepted and the transaction is finalized. The Enter function must be assigned to an actual key on the keyboard and represents a different function. Moreover, commands can be grouped together in a Command Group, e.g., Void Item, Void by Code and Void Transaction may be part of the Void Command Group.

Typically, there are two types of keys:

* **Hard Keys** - you can assign commands to hard keys. There are three types of commands:
     * Keystroke Commands such as the numbers on the keypad, paging, quantity keys, etc.
    * Regular Commands, such as Void Transaction, Price Query, etc
    * Preset Commands, such as a specific key that sells a specific item, or a department sale keys, cash tender etc.

* **Soft Keys** - these are commands (functions) that change according to the state and the mode of the POS terminal, e.g., Sale Mode, Tender Mode, Message Forms, etc. In a typical Dynakey NCR keyboard, there is a row of keys that trigger the soft keys.  Soft Keys are POS functions automatically installed with the system.

Prior to setting up your keyboards, set up your Commands and Command Groups.

On selecting a Hard Key, the command assigned to the key is triggered. For example, if you want to sell 2 of the same items, on selecting 2 from the keypad, assuming the keypad is assigned to number functions, and then the Quantity key, 2 items are recorded.

Commands are triggered only in the mode the commands are relevant. For example, if you are in the Login screen, and select the Void Transaction key, an error message is displayed as the Void Transaction function cannot be performed in the Login mode.  

In addition, you can assign a preset function to a key on the keyboard. A preset function indicates that a predefined function is automatically assigned to the key.

The following presets are available:

* **Item** - The preset key is for selling specific items by selecting a key
* **Department** - The preset key is for department sales, i.e., assign a key to invoke a department sale within a specific department as a parameter, e.g., Drinks
* **Tender** - The preset key invokes a specific tender flow, e.g., you can specify that Cash or Visa is invoked when selecting a specific key in Tender mode

On selecting a Soft Key, the command to the left of the key is triggered. For example, if the command to the left of the key is Transaction Based Return, on selecting the soft key, the system starts a transaction based return transaction. In some cases, a soft key triggers a command group, which then displays the commands within the command group. For example, a Void command group may break into Void Item, Void by Code, Void Transaction. If you are using a PC keyboard, Soft keys can be controlled with the Function buttons on the PC keyboard, i.e., F1, F2 and so on. The order in which they are displayed on the screen is defined in an XML in the initial installation.

**Reference Path:** *Organization/Devices/Keyboard Programming*

![Keyboard Programming Screen](/Images/KeyboardProgrammingScreen.png)

|**Field**|**Description**|
|---------|----------|
|Name|The name of the keyboard defined in the system, e.g. Dynakey.|
|Description|The keyboard description.|

**Reference Path:** *Organization/Devices/Keyboard Programming/Add New*

![Keyboard Programming Form](/Images/KeyboardProgrammingForm.png)

|**Field**|**Description**|
|---------|----------|
|Name|The name of the keyboard defined in the system.|
|Description|Description of the keyboard.|
|Touchpoint Type|The Touchpoint type, e.g., POS, DynaKey POS, Self Checkout, Mobile Shopper.|
|Location|The stores where the keyboard is active.|
|Touchpoint Groups|The touchpoint groups to which the keyboard applies.|
|**Key Bindings**|The bindings for different keys|
|Key Code|The unique virtual code for a key. The virtual code is the ASCII code for the numbers and letters on the keyboard. Some codes, such as the up/down arrows on the keyboard, do not have an ASCII code, only a virtual code.|
|Modifier|The modifier that applies an additional command to the key. Modifiers enable you to assign 4 commands to one key.<BR>The modifier options are: (no modifier) / Ctrl / Alt / Shift<BR>For example, you can assign key F12 to a command. You can use it for a different command by selecting Ctrl + F12.|
|Command|The function assigned to the key.|
|Parameter|The value of a specific function type, for example, if you assigned a preset item to a key, you can then specify the item number.<BR>The Parameter option is relevant to Preset Commands only.|
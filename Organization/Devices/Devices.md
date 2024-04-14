## Devices

**Devices** are the peripherals linked to the clients, e.g., EFT providers, Printers, Scanners, MSR devices, etc.

Each device must be defined with its specific attributes and then linked to the clients.

**Reference Path:** *Organization/Devices/Devices*

![Devices Screen](/Images/DevicesScreen.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of each device.|
|**Description**|Description of the device.|

**Reference Path:** *Organization/Devices/Devices/Add New*

![Devices Form](/Images/DevicesForm.png)

|**Field**|**Description**|
|---------|----------|
|**Name**|The name of the device, e.g. printer.|
|**Description**|A description of the device.|
|**Controlled by EPS**|Indicates if the device is controlled by an Electronic Payment Service (EPS), e.g. a Magnetic Stripe Reader (MSR).<BR>The options are:<BR><BR>**Yes** - the device is controlled by EPS<BR>**No** - the device is not controlled by EPS|
|**Device types**|The Device Type assigned to the device. A Device Type includes the device error codes, the correlated alert template that is triggered on each device for each alert and the methods used to handle the alert.|
|**Configuration Data**|
|Key|The Device parameters.<BR>**Note:** The **Key** and **Value** values are taken from the specifications of the manufacturer's device.<BR>Examples of keys:<BR><BR>**DeviceInfoType** – defines the type of device connected to the touch point, e.g., DrawerInfo.<BR>**IsOPOSCompliant** - defines if the device is OPOS compliant. The values are True or False. All devices are OPOS compliant.<BR>**LogicalName** - this is the logical name of the implementation component used in the POS to load the OPOS control. Usually it should be set to DEFAULT (when using the CCO standard), but there may be exceptions when applying these rules (such as the Symbol OPOS). When set to SIM, the POS will load the Device-Simulator of the relevant device, e.g., Emulator.<BR>**Timeout** - defines how many seconds after a device is idle, the device should exit for timeout. This timeout does not apply when waiting for tenders waiting for external validation. The key value must be numeric and is defined in milliseconds. For example, to indicate that timeout occurs after 5 seconds, in the Value field, enter 5000. (5 seconds).<BR>**DoubleScanPreventionTimeInterval** - defines the number of seconds in which a cashier cannot rescan an item to prevent the cashier from performing a double scan of the same item by accident. This prevents the customer from being charged double for an item by mistake. The key value must be numeric and is defined in milliseconds. For example, to indicate that an item cannot be rescanned within 2 seconds, in the Value field, enter 2000. (2 seconds).<BR>**Is Optional** - defines if the device is optional.<BR>On loading the POS, for all devices for which the IsOptional parameter is set to True that could not be initialized, a Skip button is displayed. On selecting the Skip button, the POS is loaded without the device.<BR>For the CTM device, the IsOptional parameter can be used to disable the Cash Mode on initializing the POS. On loading a touchpoint, all the devices connected to the touchpoint that were previously configured, are initialized. When the device is configured, if the IsOptional parameter is set to True, on starting the POS, if the CTM device cannot be initialized, the initialization error screen displays the Skip and Disable Cash Mode button. On selecting the button, the POS is loaded without the CTM device and the Cash Mode is disabled. This means no Cash Tenders are available on the POS and the Enable Cash Button is available.<BR>If the IsOptional parameter is set to False, on starting the POS, if the CTM device cannot be initialized, the Skip and Disable Cash Mode button is disabled and greyed out.<BR>**CMPath** - specifies the path to the Cash Management Application. This is relevant to the CTM device.<BR>**CMXmlPath** - specifies the path to the XML file containing the Add Loan and Tender Pickup Cash Office Activities performed in the Cash Management CTM Application, which are copied in to Emerald Global. This is relevant to the CTM device.<BR>**IsHighQualityLogo** - defines that the printed Logo is printed in the Highest Printer Quality. This is relevant for Printer devices.<BR>**IsPrinterDefinedLogoMaxWidth** – defines the Maximal Width that the Logo can be adjusted for the Printer Width. This is relevant for Printer devices.<BR>**IsFuelingDevice** - specifies if the device is a fuel device.<BR>For all Fuel installations, the parameter must be set to True for the following Fuel devices: COPT, Fueling Point, Forecourt, Tank.<BR>If the parameter is not configured, the RFS (Retalix fuel server) will NOT be launched.|
|Value|The value of the key.|
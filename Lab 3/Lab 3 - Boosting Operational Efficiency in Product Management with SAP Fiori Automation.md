# Lab 3 - Boosting Operational Efficiency in Product Management with SAP Fiori Automation

## Objective 

To automate Contoso Electronics' product data management and reporting
processes using Power Automate Desktop (PAD). This will assist in
handling and processing large datasets related to product inventory,
performing automated searches, and generating detailed product reports
for internal use. The automation will streamline operational efficiency,
reduce manual effort, and ensure accuracy in data reporting.

## Solution Focus Area 

Contoso Electronics, a leader in consumer electronics, maintains a vast
inventory of products. The current manual product management process,
which involves searching for product information across various
databases and generating reports, has led to several challenges:

1.  **Time-Consuming Searches**: Employees manually search through
    product data, often spending hours filtering through large datasets
    to find relevant information.

2.  **Inefficient Report Generation**: Manually generating detailed
    reports from the gathered data leads to inconsistencies, delays, and
    potential errors.

To enhance internal operational efficiency, Contoso Electronics will
implement Power Automate Desktop to automate the product search and
report generation process. The automation will reduce manual effort,
increase accuracy, and improve overall productivity.

### Estimated Time: 60 min

## Exercise 1: Create a flow and declare the variables

### Task 1: Install Power Automate Desktop

1.  Sign in with your Admin tenant credentials to Power Automate
    using <https://make.powerautomate.com/>. Click **My flows** from
    left pane. Click **Desktop flows** then click **Install \>Power
    Automate for Desktop**.

    <img src="./media/image2.png"
style="width:6.26806in;height:1.86181in" />

2.  Navigate to **File Explorer** and click **Downloads** from left pane
    then double click **Setup.Microsoft.PowerAutomate.exe**.

    <img src="./media/image3.png" style="width:6.5in;height:1.72222in"
alt="A screenshot of a computer Description automatically generated" />

3.  Click **Next** on **Install Power Automate package** pane.

    <img src="./media/image4.png"
style="width:6.26806in;height:4.65764in" />

4.  Click check box for **By selecting Install you agree to Microsoft’s
    terms of use**. Click **Install** on Installation details pane.

    <img src="./media/image5.png"
style="width:6.26806in;height:4.68333in" />

5.  Click **Yes** on Do you want to allow this app to make changes to
    your device? dialog.

    <img src="./media/image6.png" style="width:6.5in;height:3.36528in"
alt="Graphical user interface, application Description automatically generated" />

6.  Click **Launch app** on Installation successful pane.

    <img src="./media/image7.png" style="width:6.26806in;height:4.7in" />

7.  Sign in with your Admin tenant credentials.

    <img src="./media/image8.png"
style="width:6.26806in;height:7.64722in" />

8.  You will be navigated to Power Automate for Desktop Home page.

### Task 2: Create a Power Automate Desktop flow.

1.  Open the Power Automate Desktop icon from the Desktop.

    <img src="./media/image9.png" style="width:2.75857in;height:3.62531in"
alt="A screenshot of a computer Description automatically generated" />

2.  From top bar select **Dev One** environment.

    <img src="./media/image10.png" style="width:6.26806in;height:0.89653in"
alt="A computer screen with a blue and white box Description automatically generated" />

3.  To create a new flow, click on **+ New flow.**

    <img src="./media/image11.png" style="width:6.26806in;height:3.31528in"
alt="A screenshot of a computer Description automatically generated" />

4.  Name the flow as **SAP Fiori Automation.** Click on **Create**.

    <img src="./media/image12.png"
style="width:6.26806in;height:3.95694in" />

5.  The new flow gets created and opened.

    <img src="./media/image13.png"
style="width:6.26806in;height:3.73681in" />

### Task 3: Declare Input and Output variables

1.  From the right-side pane, select second icon to open **Variables**
    pane, click on the **+** icon under **Input/output variables** and
    select **Input**.

    <img src="./media/image14.png"
style="width:6.26806in;height:3.75139in" />

2.  On the New input variable pane, provide the following details and
    then click on **Save**.

    | **Property**      | **Value**                         |
    |-------------------|-----------------------------------|
    | Variable name     | SAPUserID                         |
    | Data type         | Text                              |
    | Default value     | **Enter Your SAP ES5 User ID which created in Lab 1**    |
    | External name     | SAP UserID                        |
    | Description       | SAP User ID to login to SAP Fiori |
    | Mark as Sensitive | Enable                            |

    <img src="./media/image15.png" style="width:6.26806in;height:4.95in"
alt="A screenshot of a computer Description automatically generated" />

3.  Similarly, to add an input variable, click on **+sign** next to
    Input/output variables.

    <img src="./media/image16.png"
style="width:4.51742in;height:3.6856in" />

4.  Add an input variable for Password with the following details.

    | **Property**      | **Value**                      |
    |-------------------|--------------------------------|
    | Variable name     | SAPPassword                    |
    | Data type         | Text                           |
    | Default value     | **Your SAP ES5 Password which created in Lab 1**      |
    | External name     | SAP Password                   |
    | Description       | Password to login to SAP Fiori |
    | Mark as Sensitive | Enable                         |

    <img src="./media/image17.png" style="width:6.22554in;height:4.93376in"
alt="A screenshot of a computer Description automatically generated" />

5.  Now, we can see that there are two Input variables created and
    listed under the Variables pane on the right pane.

    <img src="./media/image18.png" style="width:3.3856in;height:3.34372in"
alt="A screenshot of a computer Description automatically generated" />

6.  Now, click on the **+ icon** to add an output variable.

    <img src="./media/image19.png"
style="width:6.26806in;height:2.01597in" />

7.  Fill in the details as below and click on **Save**.

    | **Variable**  | **Property**          |
    |---------------|-----------------------|
    | Variable name | Processingresults     |
    | Data type     | Text                  |
    | External name | Result                |
    | Description   | Result of the process |

    <img src="./media/image20.png" style="width:6.22554in;height:4.55039in"
alt="A screenshot of a computer Description automatically generated" />

## Exercise 2: Add a sub flow for Exception Handling 

1.  We will add Exception handling in order to handle scenarios like
    some window is not available or any UI click event failure and so
    on.

2.  Create a **Subflow** by clicking on **SubFlows** -\> **New
    subflow.**

    <img src="./media/image21.png"
style="width:6.26806in;height:3.39931in" />

3.  Name it as **ExceptionHandler** and then click on **Save**.

    <img src="./media/image22.png" style="width:6.26806in;height:2.52083in"
alt="A screenshot of a computer Description automatically generated" />

4.  In the search bar of the Actions pane, type **Get last error** and
    double click on the action **Get last error** to add it to the
    **ExceptionHandler** subflow and click on **Save**.

    <img src="./media/image23.png"
style="width:6.26806in;height:3.48819in" />

5.  In the search bar of the Actions pane, type **Set variable** and
    double click on the action **Set variable** to add the action to the
    flow. Add the values as per the below table and click on **Save**.

    | **Property** | **Value** |
    |----|----|
    | Variable | Click on NewVar, select the **x** symbol and select the output variable – **Processingresults** |
    | Value | **\## Exception \## - %LastError%** |

    <img src="./media/image24.png"
style="width:6.26806in;height:4.02083in" />

6.  Now, add an action **Stop flow,** which will stop the flow if there
    is an error.

    Fill in the details as below and click on **Save**.

    | **Property**  | **Value**                     |
    |---------------|-------------------------------|
    | End flow      | Select **With error message** |
    | Error message | **%LastError%**               |

    
    <img src="./media/image25.png"
style="width:6.26806in;height:4.44931in" />

7.  The **ExceptionHandler** subflow should now look as in the image
    below.

    <img src="./media/image26.png" style="width:6.26806in;height:2.57847in"
alt="A screenshot of a computer Description automatically generated" />

## Exercise 3: Add a subflow to logon to SAP Fiori 

### Task 1: Create Subflow and Actions to the Logon subflow

1.  Create a **Subflow** by clicking on **SubFlows** -\> **New
    subflow.**

    <img src="./media/image27.png"
style="width:6.26806in;height:4.02847in" />

2.  Name the subflow as **SAP_Logon**. Click on **Save**.

    <img src="./media/image28.png" style="width:6.26806in;height:2.59444in"
alt="A screenshot of a computer Description automatically generated" />

3.  From the search bar of the Actions pane, type in **launch**.

    <img src="./media/image29.png" style="width:6.15278in;height:1.68056in"
alt="A screenshot of a computer Description automatically generated" />

4.  Drag and drop the **Launch new Microsoft Edge**/**Launch new
    Chrome** action on to the SAP_Logon subflow screen.

    Under Select parameters, provide the following details and then click on
**Save**.

    | **Property** | **Value** |
    |----|----|
    | Launch mode | **Launch a new instance** |
    | Initial URL | <https://sapes5.sapdevcenter.com/sap/bc/ui5_ui5/ui2/ushell/shells/abap/FioriLaunchpad.html> |
    | Window state | **Normal** |

    <img src="./media/image30.png" style="width:6.26806in;height:3.59167in"
alt="A screenshot of a computer Description automatically generated" />

    > **Note:** You can use the browser of your choice from the list available
under the Browser automation actions in the Power Automate.

    <img src="./media/image31.png" style="width:3.30862in;height:3.21695in"
alt="A screenshot of a browser Description automatically generated" />

5.  Right click on the added action and select **Run from here**.

    <img src="./media/image32.png" style="width:6.26806in;height:3.41319in"
alt="A screenshot of a computer Description automatically generated" />

6.  This opens the **Fiori login page** in a new Chrome browser.

    > **Note:** To see this log in page, check that Fiori page is not already
open on your browser. If opened, log out from the page and again run the
action.

    <img src="./media/image33.png" style="width:6.26806in;height:3.48264in"
alt="A screenshot of a computer Description automatically generated" />

7.  From here, we can record the series of events to login to the
    system. Click on **Recorder** on the Power Automate flow screen.

    <img src="./media/image34.png" style="width:6.26806in;height:2.24722in"
alt="A screenshot of a computer Description automatically generated" />

8.  The Recorder gets opened. Have the **SAP Fiori login page** open and
    click on **Record** in Recorder pane.

    <img src="./media/image35.png" style="width:6.26806in;height:3.62569in"
alt="A screenshot of a computer Description automatically generated" />

9.  Select the **User ID** field and enter the SAP User ID into that,
    Then click on **Password field** and enter SAP Password. In last
    click on the **Log On** button

    > **Note:** While logging in, ensure that the text field or the button
that you are clicking on is highlighted, to ensure that your action is
being recorded by the recorder. (Like the Logon button is highlighted
in the screenshot below).

    <img src="./media/image36.png" style="width:6.26806in;height:3.05208in"
alt="A screenshot of a computer Description automatically generated" />

10. The sequence of events of logging into the system will get recorded
    by the recorder now.

11. After recording, click on pause button place at top and look for the
    recorded value in the recorder. Click on Arrow next to **Text** and
    select **Variable**.

    <img src="./media/image37.png" style="width:2.55856in;height:5.09211in"
alt="A screenshot of a computer Description automatically generated" />

12. Once Variable is selected, select **SAPUserID** from the variable
    names.

    <img src="./media/image38.png" style="width:3.00859in;height:3.55031in"
alt="A screenshot of a computer Description automatically generated" />

13. Then change the variable name for the Password as **SAPPassword**.

14. In the Recorder window, the recorded events should look similar to
    the events in the screenshot below. Click on **Done**.

    <img src="./media/image39.png"
style="width:6.26806in;height:4.34792in" />

15. The subflow **SAP_Logon** should look similar to the one in the
    screenshot below. Click on **Save** icon to save the flow.

    <img src="./media/image40.png" style="width:6.26806in;height:3.19832in"
alt="A screenshot of a web page Description automatically generated" />

    > **Note:** If there is an extra Launch new chrome action is added, right
click on it, and select Delete. There should be only one launch action.

16. Close the chrome browser and right click on the **Launch new
    chrome** action from the **Power Automate** **SAP_Logon** sub flow
    to check if the flow is working fine.

    <img src="./media/image41.png" style="width:6.26806in;height:2.91389in"
alt="A screenshot of a computer Description automatically generated" />

17. The flow would open a new Chrome browser, type in the **User** and
    **Password** details, click on the **Logon** button and opens up the
    **SAP Fiori**.

    <img src="./media/image42.png" style="width:6.27172in;height:3.29038in"
alt="A screenshot of a computer Description automatically generated" />

18. Back in the Power Automate Desktop flow, click on the UI Elements
    icon from the right pane and select **Add UI element**.

    <img src="./media/image43.png"
style="width:6.26806in;height:5.70347in" />

19. Open the chrome browser with the **SAP Fiori** open and capture the
    UI element **Purchase EPM**. To do this hover over the Purchase EPM
    Heading. Once you get it surrounded by the **Red box**, press **Ctrl
    button** and perform a **left click** at the same time.

    <img src="./media/image44.png" style="width:5.62938in;height:2.68184in"
alt="A screenshot of a computer Description automatically generated" />

20. This will add an entry in the UI element pane. Click on **Done**.

    <img src="./media/image45.png" style="width:2.96692in;height:5.16711in"
alt="A white rectangular frame with black border Description automatically generated" />

21. Back in the Power Automate screen, right click on the added UI
    element and select **Rename.** Rename it as **Heading**.

    <img src="./media/image46.png" style="width:4.43372in;height:4.34204in"
alt="A screenshot of a computer Description automatically generated" />

    <img src="./media/image47.png" style="width:2.06597in;height:3.49874in"
alt="A screenshot of a computer Description automatically generated" />

22. Add an action, **wait for web page content** as the last step in the
    **SAP_Logon** subflow. Select **Heading** under the UI element
    option and click on **Save**.

    <img src="./media/image48.png" style="width:6.26806in;height:3.67014in"
alt="A screenshot of a computer Description automatically generated" />

23. Click on **Save** icon to save the flow. Now, we have a flow which
    will open the SAP Fiori in a new Chrome browser, will logon to the
    system and wait till the page is loaded.

24. Close the browser that is opened while testing and then check the
    flow by performing a right click on the first action and select
    **Run from here**.

## Exercise 4: Add and configure subflow SearchProductBySupplier

### Task 1: Add Sub Workflow

1.  From the Power Automate flow page, click on the **Subflows** -\> **+
    New subflow**.

    <img src="./media/image49.png" style="width:4.76841in;height:3.9984in"
alt="A screenshot of a computer Description automatically generated" />

2.  Type in the name of the subflow as **SearchProductBySupplier** and
    click on **Save**.

    <img src="./media/image50.png" style="width:6.18387in;height:2.46688in"
alt="A screenshot of a computer Description automatically generated" />

### Task 2: Capture UI Elements for Search by supplier

1.  Click on the **UI element** and select **Add UI element**.

    <img src="./media/image51.png"
style="width:5.51714in;height:3.00859in" />

2.  Now, we will open the browser in which the **SAP Fiori** is open and
    capture the **UI elements** that will be used in this flow.

3.  To capture the UI elements, select **CTRL+left click** together.

4.  First, **capture** the **Manage Products (Ctrl+left click)** option
    in the SAP Fiori page. Once the element has been added to the UI
    element picker, click on the **Manage Products** option from the web
    page again (this time we are clicking on it to navigate to the next
    page and then capture the other elements from there).

    <img src="./media/image52.png" style="width:6.26806in;height:2.98889in"
alt="A screenshot of a computer Description automatically generated" />

    > **Note:** For each of the element, we will first capture the UI element
and then click on the same from the browser to get the flow of the
execution.

5.  **Capture** the **Supplier ID (Ctrl+left click)** option, Once the
    element has been added to the UI element picker, click on the
    **Supplier ID** option from the web page again.

    <img src="./media/image53.png" style="width:6.08232in;height:2.92795in"
alt="A screenshot of a computer Description automatically generated" />

6.  **Capture** the **Search box (Ctrl+left click)** option, Once the
    element has been added to the UI element picker, type in the
    **AVANTEL** in the Search bar.

    <img src="./media/image54.png" style="width:6.26806in;height:5.09097in"
alt="A screenshot of a computer Description automatically generated" />

7.  **Capture** the **Search icon (Ctrl+left click)** option, Once the
    element has been added to the UI element picker, click on the
    **Search Icon** option from the web page again.

    <img src="./media/image55.png" style="width:6.13867in;height:2.91427in"
alt="A screenshot of a computer Description automatically generated" />

8.  **Capture** the **Check Box (Ctrl+left click)** option, Once the
    element has been added to the UI element picker, click on the
    **Check box** option from the web page again.

    <img src="./media/image56.png" style="width:6.13455in;height:2.85726in"
alt="A screenshot of a computer Description automatically generated" />

9.  **Capture** the **Select (Ctrl+left click)** option, Once the
    element has been added to the UI element picker, click on the
    **Select** option from the web page again.

    <img src="./media/image57.png" style="width:4.43001in;height:3.67364in"
alt="A screenshot of a computer Description automatically generated" />

10. **Capture** the **Go (Ctrl+left click)** option, Once the element
    has been added to the UI element picker, click on the **Go** option
    from the web page again.

    <img src="./media/image58.png" style="width:6.26806in;height:2.91875in"
alt="A screenshot of a computer Description automatically generated" />

11. The UI element picker should now have all these UI elements added.
    It should now look like the one in the screenshot below. Click on
    **Done** on the UI element picker.

    <img src="./media/image59.png" style="width:2.7509in;height:4.10551in"
alt="A screenshot of a computer Description automatically generated" />

12. Then, right click on each of the element and **Rename** it for
    easier understanding. The elements will look like below after
    renaming.

    <img src="./media/image60.png" style="width:4.24203in;height:5.35046in"
alt="A screenshot of a computer Description automatically generated" />

### Task 3: Add actions to the flow

1.  Now, we will add the elements that were captured in the Task 1
    above, to the **SearchProductBySupplier** subflow.

2.  Add an action, **Click link on web page** and select **Manage
    Products** UI element. Leave the other defaults. Click on **Save**.

    <img src="./media/image61.png" style="width:6.26806in;height:4.48472in"
alt="A screenshot of a computer Description automatically generated" />

3.  Add an action, **Click link on web page** and select **Supplier ID**
    UI element. Click on **Save**.

    <img src="./media/image62.png" style="width:5.20627in;height:3.8052in"
alt="A screenshot of a computer Description automatically generated" />

4.  Add an action, **Click link on web page** and select **Search Box**
    UI element. Click on **Save**.

    <img src="./media/image63.png" style="width:6.26806in;height:4.29861in"
alt="A screenshot of a computer Description automatically generated" />

5.  Add an action, **Populate text field on web page** and again select
    **Search Box** UI element. Under Text, type the Value to be searched
    for. Here we have used **AVANTEL**. This can be changed as per your
    preference. Click on **Save**.

    <img src="./media/image64.png" style="width:6.26806in;height:3.62153in"
alt="A screenshot of a computer Description automatically generated" />

    > **Note:** Instead of hard coding this value, we can also add an input
variable and then use the variable name here.

6.  Add an action, **Click link on web page** and select **Search icon**
    UI element. Click on **Save**.

    <img src="./media/image65.png" style="width:6.26806in;height:4.23333in"
alt="A screenshot of a computer Description automatically generated" />

7.  Add a **Wait** Action. Enter the duration as **2,** to wait for 2
    seconds for the product to get loaded based on the Search text.
    Click on **Save**.

    <img src="./media/image66.png" style="width:6.25888in;height:3.15861in"
alt="A screenshot of a computer Description automatically generated" />

8.  Add an action, **Send Keys**. Select **Tab** key from Insert
    **Special Keys -\> Misc -\> Tab**. Click on **Save**.

    <img src="./media/image67.png" style="width:6.26806in;height:4.22569in"
alt="A screenshot of a computer Description automatically generated" />

9.  Add another **Send Keys** Action and select **Space** instead of
    Tab. Click on **Save**.

    <img src="./media/image68.png" style="width:6.26806in;height:4.22569in"
alt="A screenshot of a computer Description automatically generated" />

10. Add an action, **Click link on web page** and select **Select** UI
    element.

    <img src="./media/image69.png" style="width:6.26806in;height:4.36111in"
alt="A screenshot of a computer Description automatically generated" />

11. Add an action, **Click link on web page** and select **Go Button**
    UI element.

    <img src="./media/image70.png" style="width:6.1672in;height:4.2587in"
alt="A screenshot of a computer Description automatically generated" />

12. The flow should now look as in the screenshot below.

    <img src="./media/image71.png"
style="width:6.26806in;height:4.44514in" />

13. Add an action, **Extract data from web page**. Once added, with the
    Extract data from web page open in the Power Automate flow, **open**
    the browser in which we have the selected list of products on the
    **SAP Fiori**.

14. Right click on the column name (Image) and select **Extract entire
    HTML table**.

    <img src="./media/image72.png" style="width:4.37618in;height:3.13498in"
alt="A screenshot of a computer Description automatically generated" />

15. Once the table is added, click on **Finish** in the **Extraction
    preview** pane.

    <img src="./media/image73.png"
style="width:5.67549in;height:5.46714in" />

16. Back in the Power Automate, in the **Extract data from web page**
    pane select **Store data** mode as **Excel spreadsheet** and click
    on **Save**.

    <img src="./media/image74.png" style="width:5.93385in;height:5.46714in"
alt="A screenshot of a computer Description automatically generated" />

17. Click on **Save** icon to save the flow. Now, we have a sub flow
    which will search for a specific supplier name and export all the
    products of the supplier into an Excel.

## Exercise 5: Add subflow SAP_Logoff

### Task 1: Create Sub flow SAP_Logoff

1.  We will now create a new subflow named **SAP_Logoff** to log off
    from the **SAP Fiori**.

2.  Click on **Subflows -\> + New subflow.**

    <img src="./media/image75.png" style="width:4.21703in;height:3.67532in"
alt="A screenshot of a computer Description automatically generated" />

3.  In the **Add a subflow** pane, enter the name of the subflow as
    **SAP_Logoff.** Click on **Save**.

    <img src="./media/image76.png"
style="width:6.26806in;height:2.61181in" />

4.  The created subflow gets opened in a new tab.

5.  Open the UI Element pane and click on **Add UI element**.

    <img src="./media/image77.png" style="width:4.59072in;height:3.84459in"
alt="A screenshot of a computer Description automatically generated" />

6.  **Capture** the **UI elements** to perform the **Log off** action
    from the browser.

7.  First, capture the **P – Profile** button from the top right corner
    of the browser. To capture, press Ctrl+Left click on the item to be
    captured. Once captured, an entry will be made in the UI Element
    picker.

    <img src="./media/image78.png" style="width:6.26806in;height:3.45903in"
alt="A screenshot of a computer Description automatically generated" />

8.  Capture the **close** button of the browser in the **Goodbye**
    screen.

    <img src="./media/image79.png" style="width:6.26806in;height:3.1in" />

9.  Click on **Done** in the UI element picker.

    <img src="./media/image80.png"
style="width:4.25037in;height:2.10852in" />

### Task 2: Rename UI Elements

1.  Click on the added UI element one by one and change the name for
    each of them.

2.  Select the Profile Button **UI Element** that we captured and change
    its name to **Profile Button**.

    <img src="./media/image81.png" style="width:4.1837in;height:4.80042in"
alt="A screenshot of a computer Description automatically generated" />

3.  After renaming, the list of the log off actions UI elements should
    be like the list in the screenshot below.

    <img src="./media/image82.png"
style="width:4.52539in;height:6.04219in" />

### Task 3: Add Actions to the subflow

1.  From the **Actions** pane, drag and drop a **Click link on web
    page** action to the **SAP_Logoff** subflow pane. Select the UI
    Element to be the **Profile Button**. Click on **Save**.

    <img src="./media/image83.png"
style="width:6.26806in;height:4.24375in" />

2.  Next, add an action, **Send Keys**. Enter the given below text in
    **Text to send field** and then click on the **save** button

    > {Down}{Down}{Down}{Down}{Down}{Down}{Return}{Space}

    <img src="./media/image84.png"
style="width:6.26806in;height:3.99722in" />

3.  Add an action, **Close web browser** and click on **Save** with the
    web browser instance value as **Browser**.

    <img src="./media/image85.png" style="width:6.26806in;height:3.85694in"
alt="A screenshot of a computer Description automatically generated" />

4.  Now, the subflow should look like this.

    <img src="./media/image86.png"
style="width:6.26806in;height:2.94514in" />

## Exercise 6: Configure the Main flow

1.  The main flow does not have anything in it now.

2.  We will arrange the subflows that we created in order in the main
    flow to get a complete execution.

3.  First in the Main flow, from the Actions pane, drag and drop add an
    action **On block error** into the Main flow tab.

    <img src="./media/image87.png" style="width:6.26806in;height:3.46458in"
alt="A screenshot of a computer Description automatically generated" />

4.  Name the error block as **MainExceptionBlock**. Click on **+ New
    rule -\> Run subflow.**

    <img src="./media/image88.png" style="width:6.26806in;height:4.41042in"
alt="A screenshot of a computer Description automatically generated" />

5.  In the Run subflow option that gets added, select
    **ExceptionHandler**. Click on **Save**.

    <img src="./media/image89.png" style="width:6.26806in;height:4.44028in"
alt="A screenshot of a computer error Description automatically generated" />

6.  The Main flow will now look like this.

    <img src="./media/image90.png" style="width:6.26806in;height:1.46597in"
alt="A screenshot of a computer Description automatically generated" />

7.  Next, add an action **Runsubflow.** Select SAP_Logon subflow from
    the drop down and click on **Save**.

    <img src="./media/image91.png" style="width:6.26806in;height:3.09931in"
alt="A screenshot of a computer Description automatically generated" />

    <img src="./media/image92.png" style="width:6.22554in;height:3.17528in"
alt="A screenshot of a computer Description automatically generated" />

8.  Similarly, add the 2 more actions of **Run subflow** and select
    **SearchProductBySupplier** and **SAP_Logoff** in the same order.

9.  Your main flow should now look like this.

    <img src="./media/image93.png" style="width:6.26806in;height:2.90556in"
alt="A screenshot of a computer Description automatically generated" />

10. Click on **Save**.

    <img src="./media/image94.png" style="width:6.26806in;height:2.85694in"
alt="A screenshot of a computer Description automatically generated" />

## Exercise 7: Test the Flow

1.  From the Main block, right click and select **Run from here**.

    <img src="./media/image95.png" style="width:6.26806in;height:4.75208in"
alt="A screenshot of a computer Description automatically generated" />

2.  Observe the flow that does the following.

    1.  Opens the SAP Fiori URL in a new Chrome browser.

    2.  Logs into the system providing the username and password.

    3.  Clicks on the Manage Products page.

    4.  Searches for a specific Supplier and gets the list of products
        of the supplier.

    5.  Exports the data to an excel sheet.

    6.  Logs off from the system.

    7. Closes the browser.


### Conclusion

In this lab, participants have successfully learned how to automate SAP Fiori tasks using Power Automate Desktop. They explored key concepts such as installing the Power Automate Desktop environment, creating flows, and managing variables. Additionally, they developed error handling with subflows, automated the SAP Fiori login process, and captured web UI elements to automate actions like searching for products by supplier. This exercise enhances participants' automation skills and introduces them to streamlining SAP Fiori processes efficiently through Power Automate Desktop flows.

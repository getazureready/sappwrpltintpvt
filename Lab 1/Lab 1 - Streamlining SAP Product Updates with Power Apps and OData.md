# Lab 1 - Streamlining SAP Product Updates with Power Apps and OData

## Objective 

Streamline product management and updates for Contoso Electronics by
integrating SAP with Power Apps, enabling users to access and update SAP
product data directly from a custom-built canvas app. This solution
automates the flow of product information and reduces manual data entry
by connecting to an SAP OData API and leveraging Power Automate for
seamless updates.

## Solution Focus Area: 

Contoso Electronics aims to simplify the way their product information,
such as pricing, is updated in their SAP system. Currently, updates are
made manually, leading to inefficiencies and potential errors in the
data. By integrating SAP and Power Platform, the company can create a
more efficient workflow, enabling users to access real-time product data
and make updates directly from a Power Apps canvas app.

**The key challenges addressed include:**

1.  **Manual Updates**: Product information updates in SAP are currently
    labour-intensive and prone to error, resulting in outdated or
    incorrect data.

2.  **Inefficiency in Data Access:** Users must navigate multiple
    systems to access and update product information, leading to delays
    in the process.

To address these challenges, Contoso Electronics will implement an
integrated solution using Power Apps, Power Automate, and a custom OData
connector to automate the retrieval and updating of product data in SAP.

### Estimated Time: 45 min

<br>

## Exercise 1: Create an SAP Account

### Task 1: Create an SAP Account

1.  Log into the SAP website at <https://www.sap.com> and click on the
    admin button.

    <img src="./media/image2.png"
style="width:6.26806in;height:2.90833in" />

2.  Click on **Create your SAP account.**

    <img src="./media/image3.png" style="width:6.1672in;height:3.4253in"
alt="A screenshot of a computer Description automatically generated" />

3.  Fill in your details, select the checkbox for accepting the terms
    and conditions and click on **Submit**.

    <img src="./media/image4.png" style="width:4.95043in;height:3.50864in"
alt="A screenshot of a computer screen Description automatically generated" />

4.  You will get the **Check your email and finalize your account**
    screen.

    <img src="./media/image5.png" style="width:6.26806in;height:3.125in"
alt="A screenshot of a computer Description automatically generated" />

5.  Open the email from the sender **SAP Universal ID - Notification**
    in your registered mailbox and click on **Click to activate your
    account.**

    <img src="./media/image6.png" style="width:6.26806in;height:4.04028in"
alt="A screenshot of a computer Description automatically generated" />

6.  On the next screen, create and confirm the password, select the
    check box to acknowledge the SAP Universal ID Terms of Use and then
    click on **Submit**.

    <img src="./media/image7.png" style="width:6.26806in;height:3.79375in"
alt="A screenshot of a computer Description automatically generated" />

    > **Note:** Make a note of this username and password for future use to
access the SAP related pages.

7.  You will land on the **Thank You** page.

    <img src="./media/image8.png" style="width:6.26806in;height:2.81528in"
alt="A screenshot of a computer Description automatically generated" />

8.  Close the Thank You screen.

### Task 2: Create an account for Gateway Demo System

1.  Open <https://register.sapdevcenter.com/SUPSignForms/> from your
    browser. Enter your email id (the one that you provided during the
    SAP id creation) and click on **Continue**.

    <img src="./media/image9.png" style="width:6.26806in;height:4.4375in"
alt="A screenshot of a login box Description automatically generated" />

2.  Provide the SAP login password and then click on **Sign In**.

    <img src="./media/image10.png" style="width:6.26806in;height:4.33889in"
alt="A screenshot of a login page Description automatically generated" />

3.  Click on **Accept**.

    <img src="./media/image11.png" style="width:3.842in;height:5.34213in"
alt="A screenshot of a computer Description automatically generated" />

4.  You will be taken to the SAP Gateway Demo Server page with the login
    details to the system.

5.  Select the check box to accept the Terms and conditions and then
    click on **Register**.

    <img src="./media/image12.png" style="width:5.70049in;height:5.04905in"
alt="A screenshot of a computer Description automatically generated" />

6.  Click on Show password to view the password.

    <img src="./media/image13.png" style="width:6.5in;height:5.06597in" />

7.  Check the mailbox and open the mail from <devcenter@sap.com>. Open
    the Login to the SAP Gateway WebGUI link from the email.

    <img src="./media/image14.png" style="width:6.5in;height:3.58264in"
alt="A screenshot of a computer Description automatically generated" />

8.  Login using the login details from the email.

    <img src="./media/image15.png" style="width:5.59215in;height:5.25879in"
alt="A screenshot of a login box Description automatically generated" />

9.  Change the password and click on **Change**.

    <img src="./media/image16.png" style="width:6.5in;height:5.93889in" />

    > **Note:** Make a note of this **User id** and **Password**. This will be
the login credentials for your SAP Demo system.

10. Click on **Continue**.

    <img src="./media/image17.png" style="width:6.5in;height:2.65208in"
alt="A screenshot of a computer Description automatically generated" />

11. You will get a successfully logged on screen.

    <img src="./media/image18.png" style="width:6.26806in;height:1.23958in"
alt="A close-up of a white background Description automatically generated" />

12. Click on the **Fiori Launchpad** link. This is the Fiori Launchpad
    home page, which will be your gateway to the SAP Demo System.

    <img src="./media/image19.png" style="width:6.5in;height:2.94236in" />

## Exercise 2: Create a Custom Connector (OData connection)

### Task 1: Sign Up for Microsoft Power Apps 

 

1.  Open your web browser and go to the
    <https://powerapps.microsoft.com/free/> page. 

2.  On this page, locate the **Try free** button and click on it to
    begin the sign-up process. 

    <img src="./media/image20.png"
style="width:6.26806in;height:2.97986in" />

3.  Under the "Let's get started" section, you will see a text box
    labelled **Enter your Microsoft 365 admin credential or Work-School
    Email Id**.

4.  After entering your **ID**, check the agreement box to agree to the
    terms and conditions. 

5.  Click on **Start free** to proceed. 

    <img src="./media/image21.png"
style="width:6.26806in;height:2.93472in" />

6.  If you receive a prompt stating that you already have a Microsoft
    account associated with the entered email address, select **Sign
    in**. Enter your same **ID and Password** when prompted. 

7.  After signing in, you may be prompted with an option to stay signed
    in. Select **Yes** to stay signed in for quicker access in the
    future. 

    <img src="./media/image22.png"
style="width:6.26806in;height:3.37431in" />

8.  Once you are signed in, look at the top-right corner of the screen.
    Choose the environment **Dev One.** This is important for the next
    steps, as you will need to select this environment when working in
    Power Apps. 

    <img src="./media/image23.png" style="width:6.26806in;height:0.88958in"
alt="A screenshot of a computer Description automatically generated" />

### Task 2: Create Power Apps Custom OData Connector

1.  Select **Dev One** environment.

    <img src="./media/image23.png" style="width:6.26806in;height:0.88958in"
alt="A screenshot of a computer Description automatically generated" />

2.  From the left pane, click on the **More** and then select **Discover
    all**.

    <img src="./media/image24.png"
style="width:6.26806in;height:7.31806in" />

3.  Scroll down the Discover all connection and click on **Custom
    connectors** under **Data**.

    <img src="./media/image25.png"
style="width:6.26806in;height:2.92569in" />

4.  On the Custom connector page, click on **+ New custom connector**
    and then select the **Import from Github** option.

    <img src="./media/image26.png" style="width:6.26806in;height:2.11389in"
alt="A screenshot of a computer Description automatically generated" />

5.  Select the following details in the Import from Github pane.

    1.  Connector Type - Custom

    2.  Branch – dev

    3.  Connector – SAP-ODATA-Demo

        <img src="./media/image27.png" style="width:5.17545in;height:3.75866in"
alt="A screenshot of a computer Description automatically generated" />

6.  In the SAP-ODATA-Demo page, you can see the URL of the demo system
    as in the screenshot below.

    <img src="./media/image28.png" style="width:6.26806in;height:4.21875in"
alt="A screenshot of a computer Description automatically generated" />

7.  Select **2.** **Security** from the drop down and then select
    **Edit**

    <img src="./media/image29.png" style="width:6.26806in;height:4.15625in"
alt="A screenshot of a computer Description automatically generated" />

8.  Select **Basic authentication**.

    <img src="./media/image30.png" style="width:6.26806in;height:3.74444in"
alt="A screenshot of a computer Description automatically generated" />

    > **Note:** The username and password will be the login details of your gateway demo system which we will have to provide later.

9.  The next screen **(3. Definition),** shows the available Actions
    with the connector.

    <img src="./media/image31.png"
style="width:6.26806in;height:4.76875in" />

10. The URL shows the path to the ProductSet.

    <img src="./media/image32.png" style="width:6.26806in;height:3.31944in"
alt="A screenshot of a computer Description automatically generated" />

11. Click on **Create Connector**.

    <img src="./media/image33.png" style="width:6.26806in;height:3.62292in"
alt="A screenshot of a computer Description automatically generated" />

12. Once created, the **Create connector** option gets changed to
    **Update connector**.

    <img src="./media/image34.png" style="width:6.26806in;height:3.77847in"
alt="A screenshot of a computer Description automatically generated" />

## Exercise 3: Create the Canvas App and Power Automate Flow

### Task 1: Create Canvas Power App

1.  From the Power Apps home page, select **Apps** from the left pane
    and select **Import apps.**

    <img src="./media/image35.png"
style="width:6.26806in;height:1.95833in" />

2.  Download power apps with the help of GitHub link
    <https://github.com/microsoft/PowerPlatformConnectors/blob/master/custom-connectors/SAP-ODATA-Demo/SAP%20EPM%20Products%20Demo%20Starter.msapp>
    .

    <img src="./media/image36.png"
style="width:6.26806in;height:2.83264in" />

3.  In Import app click on the **From File (.msapp)**, browse app file
    and import the app.

    <img src="./media/image37.png"
style="width:6.26806in;height:2.78819in" />

4.  The imported app looks like the given below, the app has multiple errors since we have not connected to SAP through ODATA yet. 

    <img src="./media/image38.png"
style="width:6.26806in;height:3.94722in" />

5.  From the left pane, select **Data** then click on **+ Add data**.
    Search for OData and then select **SAP-ODATA-Demo** from it.

    <img src="./media/image39.png" style="width:6.26806in;height:4.21806in"
alt="A screenshot of a computer Description automatically generated" />

6.  Provide the login credentials of your Demo Gateway system. Click on
    **Got it** under the Premium dialog.

    <img src="./media/image40.png" style="width:3.37529in;height:5.00877in"
alt="A screenshot of a login box Description automatically generated" />

    <img src="./media/image41.png" style="width:4.9921in;height:2.34187in"
alt="A screenshot of a computer Description automatically generated" />

7.  Once the connection is made, all the errors except for one will
    have been resolved. Click on **Gallery3** from Tree view. Select
    **Advanced** tab from the **Gallery** Pane.

    <img src="./media/image42.png"
style="width:6.26806in;height:3.52569in" />

8.  Select the formula under **DATA -\> Items**. Replace the formula
    with the below one.

    > SortByColumns(zProducts, "Name")



    <img src="./media/image43.png" style="width:5.25694in;height:2.91806in"
alt="A screenshot of a computer Description automatically generated" />

9.  Save the app and click on the **Play** button.

    <img src="./media/image44.png"
style="width:6.26806in;height:0.75972in" />

10. Click on the **Refresh icon** of the Products on the app. Here, we can
    find the list of all the products from the demo SAP System, that we
    browsed through the Fiori launchpad.

    <img src="./media/image45.png" style="width:6.26806in;height:3.52014in"
alt="A screenshot of a computer Description automatically generated" />

11. Click on any item to view their values on the right-side pane. The
    app is now without any errors.

    <img src="./media/image46.png" style="width:6.26806in;height:3.48958in"
alt="A screenshot of a computer Description automatically generated" />

12. Click on **10” Portable DVD player** from the Products list. Do some
    update to the Price and click on the Tick mark. When clicked, we get
    an error message,

    > TODO: Fix the “OnSelect” formula to invoke a flow. This is because we have not defined UpdateButton yet.

    <img src="./media/image47.png" style="width:6.26806in;height:3.52292in"
alt="A screenshot of a computer Description automatically generated" />

13. From the top right corner close the app.

    <img src="./media/image48.png" style="width:6.26806in;height:3.66181in"
alt="A screenshot of a computer Description automatically generated" />

### Task 2: Add a Power Automate flow

1.  Select the **Power Automate** button from the left pane and then
    select **Create new flow**.

    <img src="./media/image49.png" style="width:6.26806in;height:5.46181in"
alt="A screenshot of a computer Description automatically generated" />

2.  On the Create your flow pane, select **+ Create from blank.**

    <img src="./media/image50.png" style="width:6.26806in;height:3.91352in"
alt="A screenshot of a computer Description automatically generated" />

3.  The flow pane gets opened click on **PowerApps(V2)**. Select **+ Add
    an input** \> **Text**.

    <img src="./media/image51.png" style="width:6.26806in;height:3.30903in"
alt="A screenshot of a computer Description automatically generated" />

4.  Enter the name as **ProductID**.

    <img src="./media/image52.png" style="width:6.26806in;height:2.12153in"
alt="A screenshot of a computer Description automatically generated" />

    Similarly, add the following as in the screenshot below.

    | **Property** | **Data Type** |
    |--------------|---------------|
    | Name         | Text          |
    | Description  | Text          |
    | E-Tag        | Text          |
    | Price        | Number        |


    <img src="./media/image53.png" style="width:4.57215in;height:3.63959in"
alt="A screenshot of a computer Description automatically generated" />

5.  Rename the flow as **UpdateProduct** and then click on **+ New
    step**.

    <img src="./media/image54.png" style="width:6.26806in;height:1.23194in"
alt="A screenshot of a computer Description automatically generated" />

6.  In the New step, select **Custom** under choose an operation and
    then select the **SAP-ODATA-Demo**.

    <img src="./media/image55.png" style="width:6.18387in;height:5.09211in"
alt="A screenshot of a computer Description automatically generated" />

7.  Enter the SAP ES5 Username and Password and click on **Create**.

    <img src="./media/image56.png" style="width:6.26806in;height:4.36667in"
alt="A screenshot of a computer Description automatically generated" />

8.  Select **Get product** from the SAP-OData-Demo.

    <img src="./media/image57.png" style="width:5.21712in;height:5.30879in"
alt="A screenshot of a computer Description automatically generated" />

9.  Under Get product, type **HT-2000** in the ID field and select
    **fetch** under x-csrf-token and then select **+ New step**.

    <img src="./media/image58.png" style="width:6.26806in;height:3.79167in"
alt="A screenshot of a computer Description automatically generated" />

10. In the New step, select **Customer \> SAP-O-DATA** and then select
    **Update product**.

    <img src="./media/image59.png"
style="width:5.17545in;height:5.36713in" />

11. Once added, select the **Product ID** field and select the **Product
    ID** that we added under the trigger, Power Apps(V2).

    <img src="./media/image60.png" style="width:6.26806in;height:4.25486in"
alt="A screenshot of a computer Description automatically generated" />

12. For the x-csrf-token, add **x-xsrf-token**.

    <img src="./media/image61.png"
style="width:6.26806in;height:4.10694in" />

13. For **x-ms-cookie-header,** click on the Expression tab and then
    paste the below content.

    > replace(outputs('Get_product')\['headers'\]\['Set-Cookie'\],',',';')


    <img src="./media/image62.png" style="width:6.26806in;height:3.14514in"
alt="A screenshot of a computer Description automatically generated" />

14. Select the values for the Properties as below.

    | **Property** | **Value**                   |
    |--------------|-----------------------------|
    | E-Tag        | PowerApps(V2) – E-Tag       |
    | Name         | PowerApps(V2) - Name        |
    | Description  | PowerApps(V2) - Description |
    | Price        | PowerApps(V2) - Price       |

    <img src="./media/image63.png" style="width:6.26806in;height:6.67361in"
alt="A screenshot of a computer Description automatically generated" />

15. From the top bar click on **Save** button.

    <img src="./media/image64.png"
style="width:6.26806in;height:3.90278in" />

16. Once saved, click on the **Close** button.

    <img src="./media/image65.png" style="width:6.26806in;height:1.83889in"
alt="A screenshot of a computer Description automatically generated" />

### Task 3: Invoke the flow

1.  Back in the Power Apps screen, you will see that the flow is now
    added to the app.

    <img src="./media/image66.png" style="width:6.26806in;height:4.00972in"
alt="A screenshot of a computer Description automatically generated" />

2.  Got to components click on the tick button and go to Advanced
    option, In Advanced option enter the below given formula in
    OnSelect.

    > UpdateProduct.Run(*ProductBox*.Product.ProductID,*ProductNameTB*.Text,*DescriptionTB*.Text,*ProductBox*.Product.\_\_metadata.etag,*PriceTB*.Text



    <img src="./media/image67.png"
style="width:6.26806in;height:2.63472in" />

3.  Click on **Save** and then click on the **Screens** tab under the
    **Tree view**.

    <img src="./media/image68.png" style="width:6.26806in;height:1.59444in"
alt="A screenshot of a computer Description automatically generated" />

## Exercise 4: Test and check the App and Flow

### Task 1: App Testing

1.  Click on **Play**.

    <img src="./media/image69.png" style="width:6.26806in;height:1.5in"
alt="A screenshot of a computer Description automatically generated" />

    > Select the product, **10” Portable DVD player.** Change the Price on
the right-side pane of the app to **349.99** from 449.99. Click on the
**Tick Mark (UpdateButton)**. This action should trigger the
**UpdateProducts** Power Automate flow.

    <img src="./media/image70.png"
style="width:6.26806in;height:3.51597in" />

### Task 2: Check the flow and updates

1.  Go to the Power Automate page at <https://make.powerautomate.com/>

2.  Click on **My flows** and select **UpdateProducts**. Under the
    28-day run history, you can find the flow that you just triggered
    and find that the flow has succeeded.

    <img src="./media/image71.png" style="width:6.26806in;height:3.95139in"
alt="A screenshot of a computer Description automatically generated" />

3.  Open the link of the Fiori launchpad
    <https://sapes5.sapdevcenter.com/sap/bc/ui5_ui5/ui2/ushell/shells/abap/FioriLaunchpad.html#Shell-home>
    from the browser. Select the **Manage Products** tile.

    <img src="./media/image72.png" style="width:6.26806in;height:2.85903in"
alt="A screenshot of a computer Description automatically generated" />

4.  Click on **Go** and observe that the Price of the Product 10”
    Portable DVD player has been updated from 449.99 to 349.99.

    <img src="./media/image73.png" style="width:6.26806in;height:2.62847in"
alt="A screenshot of a computer Description automatically generated" />

### Conclusion

In this lab, participants learned how to integrate SAP with Microsoft Power Platform by creating an SAP account and accessing the SAP Gateway Demo System. They configured a custom OData connector to link SAP data with Power Apps, built a Canvas App to display and update product information, and created a Power Automate flow to automate product updates. The lab concluded with testing the app and flow, verifying updates in the SAP Fiori Launchpad, equipping participants with key skills for SAP-Power Platform integration.

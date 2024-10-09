# SAP and Microsoft Teams Integration with Copilot and Generative AI

<table>
<colgroup>
<col style="width: 21%" />
<col style="width: 78%" />
</colgroup>
<thead>
<tr>
<th>Description </th>
<th><p>In this lab, participants will start by creating an SAP account
and setting up a Gateway Demo System to access SAP services. The next
step involves configuring Microsoft Copilot Studio and creating a
Copilot with generative AI capabilities tailored for SAP product
integration. Participants will then create Power Automate flows for
querying product information from SAP and updating product prices. These
flows will be integrated with the Copilot, allowing users to interact
with SAP through Microsoft Teams. Finally, the lab will conclude with
testing the Copilot within Teams by retrieving product information and
updating product prices, followed by verification of the updates in the
SAP system.</p>
<p> </p></th>
</tr>
</thead>
<tbody>
<tr>
<td>Prerequisites </td>
<td><p>To get the most out of this lab guide we recommend you have Work
or school Email ID-Password, Microsoft copilot Trial License, Microsoft
Teams Trial Licence, Microsoft Power Automate trial license.</p>
<p> </p></td>
</tr>
<tr>
<td>Duration </td>
<td>1 hours </td>
</tr>
<tr>
<td>Version </td>
<td>1.0 </td>
</tr>
<tr>
<td>Publication date  </td>
<td>October 2024 </td>
</tr>
</tbody>
</table>

<br>
<br>

# Exercise 1: Create SAP Account

## 

## Task 1: Create SAP Account

- Log into the SAP website at <https://www.sap.com> and click the
  **admin** button.

  <img src="./media/image1.png" style="width:6.26806in;height:2.82847in" />

- Click on **Create your SAP account.**

  <img src="./media/image2.png" style="width:6.16667in;height:3.425in" alt="A screenshot of a computer Description automatically generated" />

- Fill in your details, select the checkbox for accepting the terms and
  conditions and click on **Submit**.

  <img src="./media/image3.png" style="width:4.95in;height:3.50833in" alt="A screenshot of a computer screen Description automatically generated" />

- You will get the **Check your email and finalize your account**
  screen.

  <img src="./media/image4.png" style="width:6.26806in;height:3.12153in" alt="A screenshot of a computer Description automatically generated" />

- Open the email from the sender **SAP Universal ID - Notification** in
  your registered mailbox and click on **Click to activate your
  account.**

  <img src="./media/image5.png" style="width:6.26667in;height:4.04167in" alt="A screenshot of a computer Description automatically generated" />

- On the next screen, enter the password, select the check box to
  acknowledge the SAP Universal ID Terms of Use and then click on
  **Submit**.

  <img src="./media/image6.png" style="width:6.26667in;height:3.79167in" alt="A screenshot of a computer Description automatically generated" />

  > **Note:** Make a note of this username and password for future use to access the SAP related pages.

- You will land on the **Thank You** page.

  <img src="./media/image7.png" style="width:6.26667in;height:2.81667in" alt="A screenshot of a computer Description automatically generated" />

- Close the Thank You screen.

## Task 2: Create an account for Gateway Demo System

- Open <https://register.sapdevcenter.com/SUPSignForms/> from your
  browser. Enter your email id (the one that you provided during the SAP
  id creation) and click on **Continue**.

  <img src="./media/image8.png" style="width:6.26667in;height:4.44167in" alt="A screenshot of a login box Description automatically generated" />

  <img src="./media/image8.png" style="width:6.26667in;height:4.44167in" alt="A screenshot of a login box Description automatically generated" />

- Provide the SAP login password and then click on **Sign In**.

  <img src="./media/image9.png" style="width:6.26667in;height:4.34167in" alt="A screenshot of a login page Description automatically generated" />

- Click on **Accept**.

  <img src="./media/image10.png" style="width:3.84167in;height:5.34167in" alt="A screenshot of a computer Description automatically generated" />

- You will be taken to the SAP Gateway Demo Server page with the login
  details to the system.

- Select the check box to accept the Terms and conditions and then click
  on **Register**.

  <img src="./media/image11.png" style="width:5.7in;height:5.05in" alt="A screenshot of a computer Description automatically generated" />

- Click on **Show password** to view the password.

  <img src="./media/image12.png" style="width:6.26806in;height:4.88611in" />

- Check the mailbox and open the mail from <devcenter@sap.com>. Open the
  Login to the **SAP Gateway WebGUI** link from the email.

  <img src="./media/image13.png" style="width:6.26806in;height:3.45556in" alt="A screenshot of a computer Description automatically generated" />

- Login using the login details from the email.

  <img src="./media/image14.png" style="width:5.59167in;height:4.07576in" alt="A screenshot of a login box Description automatically generated" />

- Change the password and click on **Change**.

  <img src="./media/image15.png" style="width:6.26806in;height:5.72153in" />


> **Note:** Make a note of this **User ID** and **Password**. This will be the login credentials for your SAP Demo system.

- Click on **Continue**.

  <img src="./media/image16.png" style="width:6.26806in;height:2.55556in" alt="A screenshot of a computer Description automatically generated" />

- You will get a successfully logged on screen.

  <img src="./media/image17.png" style="width:6.26667in;height:1.24167in" alt="A close-up of a white background Description automatically generated" />

- Click on the **Fiori Launchpad** link. This is the Fiori Launchpad
  home page, which will be your gateway to the SAP Demo System.

  <img src="./media/image18.png" style="width:6.26806in;height:2.83681in" />

# Exercise 2: Create and Configure Copilot

## Task 1: Login in Copilot studio

- Navigate to
  <https://www.microsoft.com/en-us/microsoft-copilot/microsoft-copilot-studio>
  and click on **Sign in** button.

  <img src="./media/image19.png"
style="width:6.26806in;height:2.87083in" />

- Enter the login **admin tenant login ID / Work-School ID** and click
  on the Next. For this lab we use **Admin tenant ID and Password.**

  <img src="./media/image20.png"
style="width:6.26806in;height:3.23472in" />

- Enter the **Admin tenant Password** and click on the **Sign In**
  button.

  <img src="./media/image21.png"
style="width:6.26806in;height:3.10833in" />

- Select **yes** for stayed sign in with credential.

  <img src="./media/image22.png"
style="width:6.26806in;height:3.80972in" />

## Task 2: Create a Copilot with Gen AI Capabilities

- Opne Copilot studio and from top environment sections select **Dev
  One** environment.

  <img src="./media/image23.png"
style="width:6.26806in;height:2.84931in" />

- Click on the **Create** button form the left navigation bar and then
  select **New Copilot** option.

  <img src="./media/image24.png"
style="width:6.26806in;height:2.65417in" />

- Click on the **Skip to configure** and start manual configuration of
  copilot.

  <img src="./media/image25.png"
style="width:6.26806in;height:2.64306in" />

- Enter the following details in the respected fields and click on the
  **Create** button.

  - **Name:** SAP Product Copilot

  - **Description:** The Copilot allows you to integrate SAP system and
    fetch product information live from SAP and update price of
    products.

  - **Instructions:** The copilot has to check the available product in
    SAP system and provide the product information as per the
    requirement and update the price of the product.

  <img src="./media/image26.png"
style="width:6.26806in;height:2.80069in" />

- Click on the **Setting** form the top right corner and then select
  **Generative AI** option. In Generative AI setting select **Generative
  AI (Preview)** and select **Medium** content moderation. After the
  configuration click on the save button.

  <img src="./media/image27.png"
style="width:6.26806in;height:2.62222in" />

# Exercise 3: Create Power Automate Flow for SAP Integration

## Task 1: Create Power Automate Flow for Product Information

- Then go back to overview section of copilot and select **Actions**
  from the top bar. After click on actions select **Add an action**
  button to create a new SAP action.

  <img src="./media/image28.png"
style="width:6.26806in;height:3.32153in" />

- Scroll down select **Choose an action section** and click on **Create
  a new flow** button, it will redirect to power automate flow.

  <img src="./media/image29.png"
style="width:6.26806in;height:3.67847in" />

- From top left corner rename the flow as **SAP Product Category**.

  <img src="./media/image30.png"
style="width:6.26806in;height:2.63056in" />

- Click on the **Run a flow from copilot** and select **+ Add an
  input**.

  <img src="./media/image31.png"
style="width:6.26806in;height:2.74931in" />

- In **+ Add an input** option select **Text** as type of input.

  <img src="./media/image32.png"
style="width:6.26806in;height:2.73333in" />

- Enter **Product Input** in the input section.

  <img src="./media/image33.png"
style="width:6.26806in;height:2.38333in" />

- Click on the **+** sign and select **Add an action** option.

  <img src="./media/image34.png"
style="width:6.26806in;height:2.65833in" />

- In Add an action section enter **SAP OData** and select **Query OData
  entities.**

  <img src="./media/image35.png"
style="width:6.26806in;height:3.45417in" />

- Enter the following Details in the Create a new connection section and
  then click on the **Create new button**.

  - **Connection Name:** SAP-Product-100

  - **Authentication Type:** Basic

  - **OData Base URL:**
    <https://sapes5.sapdevcenter.com/sap/opu/odata/iwbep/GWSAMPLE_BASIC>

  - **User Name:** Enter the ES5 SAP User ID which we created in
    exercise 1 task 2.

  - **Password:** Enter the ES5 SAP Password which we created in
    exercise 1 task 2.

  <img src="./media/image36.png"
style="width:6.26806in;height:5.86736in" />

- In **OData Entity Name** select **Productset** and then click on
  **Show all.**

  <img src="./media/image37.png"
style="width:6.26806in;height:2.07153in" />

- In **\$Top** section enter **10,** which will return top 10 product.

  <img src="./media/image38.png"
style="width:6.26806in;height:1.36111in" />

- Click on the **Respond to Copilot** option and click on **Add an
  output** option.

  <img src="./media/image39.png"
style="width:6.26806in;height:2.51875in" />

- Select **Text** as type of output.

  <img src="./media/image40.png"
style="width:6.21721in;height:2.68357in" />

- Enter **Product Output** as output name and then enter the
  **string(body('Query_OData_entities'))** as the value of the output
  with the help of function. Click on the Add button after enter the
  output query.

  <img src="./media/image41.png" style="width:6.26806in;height:3.775in" />

- **Save** and **Publish** the copilot.

  <img src="./media/image42.png"
style="width:6.26806in;height:2.66111in" />

- Go back to copilot studio and click on the **Refresh**.

  <img src="./media/image43.png"
style="width:6.26806in;height:4.19931in" />

## Task 2: Create Power Automate Flow for Update Product

- On the **Choose an action** window scroll down and click on the
  **Create a new flow.**

  <img src="./media/image44.png"
style="width:6.26806in;height:4.13819in" />

- Rename the Flow Name as **Update Product Price.**

  <img src="./media/image45.png"
style="width:6.26806in;height:2.64514in" />

- Click on the **Run a flow from copilot** and then select **+ Add an
  input.**

  <img src="./media/image46.png"
style="width:6.26806in;height:3.29722in" />

- Select the type of user input as **Text**.

  <img src="./media/image47.png"
style="width:6.26806in;height:3.40069in" />

- Rename the input name as **Product ID.**

  <img src="./media/image48.png"
style="width:6.26806in;height:3.12222in" />

- Then again click on the + Add an input, select **Number** as input
  type and rename the input as **Update Price.**

  <img src="./media/image49.png"
style="width:6.26806in;height:3.01458in" />

- Click on the **+** Icon and select **Add an action.**

  <img src="./media/image50.png"
style="width:6.26806in;height:2.49514in" />

- Enter **SAP OData** in the Add an action search bar and click on **see
  more**.

  <img src="./media/image51.png"
style="width:6.26806in;height:4.15694in" />

- Click on the **Update OData entity**. After click on the entity, it
  will connect automatically with SAP OData Connection which we create
  in **SAP Product Category** flow.

  <img src="./media/image52.png"
style="width:6.26806in;height:4.24653in" />

- Click on the OData Entity Name and select **ProductSet.**

  <img src="./media/image53.png"
style="width:6.26806in;height:2.03194in" />

- In the ProductID sections select **ProductID** with the help of
  dynamic content.

  <img src="./media/image54.png"
style="width:6.26806in;height:2.24236in" />

- Click on the **Advanced parameters** and select **Price**.

  <img src="./media/image55.png"
style="width:6.26806in;height:1.68819in" />

- In the price parameter enter **Update Price** with the help of dynamic
  content.

  <img src="./media/image56.png"
style="width:6.26806in;height:2.29306in" />

- Click on the **Save and draft** and then click on **Publish**.

  <img src="./media/image57.png"
style="width:6.26806in;height:2.56389in" />

# Exercise 4: Integrate Power Automate Flow with Copilot

## Task 1: Integrate SAP Product Category Flow

- Go back to copilot studio window and click on the **Refresh** button.

  <img src="./media/image58.png"
style="width:6.26806in;height:2.51597in" />

- Scroll down choose an action window and select **SAP Product
  Category** flow.

  <img src="./media/image59.png"
style="width:6.26806in;height:3.21389in" />

- Click on the next button.

  <img src="./media/image60.png"
style="width:6.26806in;height:3.85972in" />

- In the Input Parameter click on the edit input button and add the
  description as given below and the click on save button.

**Description:** Product Category. One of the following categories can
be used. The name has to be exactly like this: Accessories, Notebooks,
Laser Printers, Mice, Keyboards, Mousepads, Scanners, Speakers,
Headsets, Software, PCs, Smartphones, Tablets, Servers, Projectors, MP3
Players, Camcorders.

  <img src="./media/image61.png"
style="width:6.26806in;height:2.76528in" />

  <img src="./media/image62.png"
style="width:6.26806in;height:3.59861in" />

- Click on the outputs and then select edit outputs.

  <img src="./media/image63.png"
style="width:6.26806in;height:1.25903in" />

- Enter the given below given description and click on the save button.

**Description:** List of SAP products for a provided product category.
Return the result as table including following information: ProductID,
Category, Name, Description and Price.

  <img src="./media/image64.png"
style="width:6.26806in;height:3.99375in" />

- Click on the **Next** button and after that click on the **Finish** to
  complete the configuration.

  <img src="./media/image65.png"
style="width:6.26806in;height:4.01111in" />

  <img src="./media/image66.png"
style="width:6.26806in;height:3.83125in" />

- Go to action section and the select the SAP Product Category action.

  <img src="./media/image67.png"
style="width:6.26806in;height:2.09583in" />

- Go to **Output** section and check the box **Respond to the user after
  running this action**. After check the box click on the save button.

  <img src="./media/image68.png"
style="width:6.26806in;height:3.47361in" />

- Click on the Test Button place as the top right side and enter the
  prompt Notebooks in the respected field. It will return the connect
  request. Click on the connect to give the permission. After select
  connect, it will redirect to connection window.

  <img src="./media/image69.png"
style="width:6.26806in;height:2.48958in" />

- In Manage your connections window click on the connect button.

  <img src="./media/image70.png"
style="width:6.26806in;height:2.20278in" />

- Click on the three dots on SAP OData and select **SAP-Product-100**
  connection. After selecting the connection click on the Submit button.

  <img src="./media/image71.png"
style="width:6.26806in;height:4.30069in" />

- Flow is shown as connected in the Manage connections.

  <img src="./media/image72.png"
style="width:6.26806in;height:1.98681in" />

## Task 2: Create topic Product Update

- Go to topic for the top bar and click on the **Add new topic** and
  then click on **From** **blank**.

  <img src="./media/image73.png"
style="width:6.26806in;height:1.63403in" />

- Rename the topic as **Product Update**.

  <img src="./media/image74.png"
style="width:6.26806in;height:2.45625in" />

- In the trigger node, Enter the below given description.

Update Product, Update Product Price, Update Price, Price Update

  <img src="./media/image75.png"
style="width:5.09489in;height:2.19464in" />

- Below trigger node, add **Message Node.**

  <img src="./media/image76.png"
style="width:4.85042in;height:3.40029in" />

- Enter the message in the Message Node which is given below.

Thank you for using our service. Please enter **Product ID** and
**Update Price** in below given card.

  <img src="./media/image77.png"
style="width:4.68374in;height:1.80016in" />

- Click on the + Sign below message node and add Ask with adaptive card
  node.

  <img src="./media/image78.png"
style="width:6.26806in;height:4.44444in" />

- Click on the three dots on adaptive card and click on the properties.

  <img src="./media/image79.png"
style="width:6.26806in;height:2.85972in" />

- Enter the below give code in the properties window and close the
  properties.

""

{

"type": "AdaptiveCard",

"\$schema": "http://adaptivecards.io/schemas/adaptive-card.json",

"version": "1.3",

"body": \[

{

"type": "Input.Text",

"placeholder": "Placeholder text",

"id": "1",

"label": "Product ID"

},

{

"type": "Input.Number",

"placeholder": "Placeholder text",

"id": "2",

"label": "Updated Price"

},

{

"type": "ActionSet",

"actions": \[

{

"type": "Action.Submit",

"title": "Submit"

}

\]

}

\]

}

""

  <img src="./media/image80.png"
style="width:6.26806in;height:3.56389in" />

- Below adaptive card output section is available, in output **section
  1** variable click on select a variable and then click on the create
  new, a new variable **Var1** is created.

  <img src="./media/image81.png"
style="width:6.26806in;height:2.44722in" />

- Repeat same process for next output Var2 is created.

  <img src="./media/image82.png"
style="width:4.51706in;height:2.6669in" />

- Go to variable from the top and select all right side check box for
  all variable.

  <img src="./media/image83.png"
style="width:6.26806in;height:3.05694in" />

- Below adaptive card, click on + sign and select call an action, then
  select **Update Product** flow.

  <img src="./media/image84.png"
style="width:6.26806in;height:3.38542in" />

- In the Action select Var1 for Product ID and Var2 for Update Price.

  <img src="./media/image85.png"
style="width:6.26806in;height:3.06667in" />

  <img src="./media/image86.png"
style="width:5.84217in;height:3.34196in" />

- Below Action node, click on + sign and add Message node, in message
  node enter the flowing message. **Product Var1 price is updated.
  Thankyou.** Replace Var1 with Variable name Var1 with the help of {x}
  button.

  <img src="./media/image87.png"
style="width:6.26806in;height:2.79583in" />

- Click on the Test button and enter the prompt Update Price. Then fill
  the Product ID (HT-1001) and price (1540), click on submit. After
  click on submit a message show to connect. Click on the connect.

  <img src="./media/image88.png"
style="width:6.26806in;height:4.69931in" />

- It will navigate to other window which manage the connections. Click
  on the connect button of Update Product Price.

  <img src="./media/image89.png"
style="width:6.26806in;height:1.86389in" />

- Click on the three dots and select connection SAP-Product-100 then
  click on submit button.

  <img src="./media/image90.png"
style="width:6.26806in;height:2.71458in" />

- After the completing it shows connected.

  <img src="./media/image91.png" style="width:6.26806in;height:2.075in" />

- Click on the publish button to save the copilot setting

  <img src="./media/image92.png"
style="width:5.0171in;height:2.01684in" />

# Exercise 5: Integrate Copilot with SAP

- Go to Channels from the top bar which is placed next to Analytics and
  then click on **Microsoft Teams**.

  <img src="./media/image93.png"
style="width:6.26806in;height:3.62569in" />

- Then click on the **Turn on Teams** button.

  <img src="./media/image94.png"
style="width:2.82224in;height:3.01735in" />

- Now teams are connected successfully, now click on the **Open
  Copilot** a new window will open.

  <img src="./media/image95.png"
style="width:6.26806in;height:1.82431in" />

- On the new window click on the Use the web app instead.

  <img src="./media/image96.png"
style="width:6.26806in;height:3.56736in" />

- Now Teams app web app will open, click on the **Add** button to add
  the copilot. And then the chat bot is ready.

  <img src="./media/image97.png"
style="width:6.26806in;height:2.07014in" />

# Exercise 6: Test Copilot in teams.

- Open teams app and enter the prompt **Give me information about
  Notebooks.**

**Note:** If prompted Additional permissions are required to run this
action. To proceed, please select 'Connect', and review any missing
connections. Click on connect and apply the same steps as we perform
before. After connection created back to teams and then type prompt
again.

  <img src="./media/image98.png"
style="width:6.26806in;height:0.35417in" />

- It returns the information of the Notebooks from SAP System.

  <img src="./media/image99.png"
style="width:6.26806in;height:3.32222in" />

- Then give another prompt, I want to update price of product.

  <img src="./media/image100.png"
style="width:6.26806in;height:0.57083in" />

- Now it returns the adaptive card, enter Product ID HT-1001 and in
  price enter 1111 and then click on the submit.

  <img src="./media/image101.png"
style="width:4.10036in;height:2.14185in" />

**Note:** If prompted Additional permissions are required to run this
action. To proceed, please select 'Connect', and review any missing
connections. Click on connect and apply the same steps as we perform
before. After connection created back to teams and then type prompt
again.

- After entering the Product ID and Price confirmation message appears.

  <img src="./media/image102.png"
style="width:4.43372in;height:0.76673in" />

- To confirm the updation, go to <https://sapes5.sapdevcenter.com/> ,
  click on Fiori Launch, login with your User Id and Password, Click on
  manage product. Then in search bar type HT-1001 and then click go.

  <img src="./media/image103.png"
style="width:6.26806in;height:1.72014in" />

- Now see the updated price of the product is 1111.

  <img src="./media/image104.png"
style="width:6.26806in;height:1.47778in" />

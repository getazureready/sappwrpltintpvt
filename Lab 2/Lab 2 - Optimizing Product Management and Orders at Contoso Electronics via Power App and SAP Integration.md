# Lab 2 - Optimizing Product Management and Orders at Contoso Electronics via Power App and SAP Integration

## Objective

Contoso Electronics, a leading retail company, is looking to streamline
its product management process to improve efficiency and enhance
customer experience. The company wants to create a Power App that
integrates with its SAP backend system to provide employees with easy
access to product information, manage inventory, and facilitate customer
orders.

### Solution Focus are

Contoso Electronics, a leading retail company, aims to enhance its
product management processes by developing a Power App integrated with
its SAP backend. This solution focuses on streamlining product
information management and order processing to improve operational
efficiency and customer experience.

1.  **Power Apps Development:** The initiative will leverage a
    user-friendly interface to enable employees to access and manage
    real-time product data from SAP using OData connectors. Features
    such as a dynamic product catalogue and detailed product insights will
    empower the sales team to quickly find necessary information and
    facilitate smoother order management.

2.  **Real-Time Data Integration and Reporting:** By ensuring real-time
    updates from the SAP system, the solution will enhance data accuracy
    and provide robust reporting capabilities. This will allow the sales
    and inventory management teams to track performance metrics, monitor
    stock levels, and make informed decisions, ultimately leading to
    faster order processing and improved customer satisfaction.

### Estimated Time : 45 mins


## Exercise 1: Login and Create OData Connection Power Apps

### Task 1: Sign In into Power Apps

1.  Navigate to the power apps page and from the top right corner click on the
    **Sign in** button.

    <img src="./media/image2.png"
style="width:6.26806in;height:2.95903in" />

2.  Enter the admin tenant id and then click on the **Next** button.

    <img src="./media/image3.png"
style="width:6.26806in;height:2.92083in" />

3.  Enter the password in the respected field and then click on the
    **Sign** **in** button.

    <img src="./media/image4.png"
style="width:6.26806in;height:2.66319in" />

4.  **Check** the Don’t show this again box and click on the **Yes** to
    stay signed in.

    <img src="./media/image5.png"
style="width:6.26806in;height:2.68681in" />

5.  After Login From the top bar chose the developer **environment**. In
    our case **Dev One** is a development environment.

    <img src="./media/image6.png"
style="width:5.91057in;height:2.71168in" />

### Task 2: Create SAP OData Connection

1.  From the left Navigation bar select **More** and then click on the
    **Connections.**

    <img src="./media/image7.png"
style="width:6.26806in;height:2.63333in" />

2.  Then from the top bar click on the **+ New Connection.**

    <img src="./media/image8.png"
style="width:6.26806in;height:2.65556in" />

3.  Search SAP OData in the search bar from top right corner and then
    select **SAP OData.**

    <img src="./media/image9.png"
style="width:6.26806in;height:1.97569in" />

4.  Enter the following details in the SAP OData configuration window.

    | Authentication Type | Basic |
    |----|----|
    | OData Base URL | <https://sapes5.sapdevcenter.com/sap/opu/odata/iwbep/GWSAMPLE_BASIC> |
    | User Name | Enter SAP ES5 P-ID (we created in Lab 1) |
    | Password | Enter SAP ES5 P-Password (we created in Lab 1) |

    <img src="./media/image10.png"
style="width:6.26806in;height:3.13403in" />

5.  The New Connection is created now, click on the three dots (…) of
    the connection and select **Edit**. Rename the Display Name as
    **Contoso-Product**. Enter again the same P ID and Password and click on
    **Save**.

    <img src="./media/image11.png"
style="width:6.26806in;height:3.44167in" />

## Exercise 2: Create and Configure Contoso Power App


### Task 1: Create Contoso Power apps

1.  From the left-hand navigation bar select on the **+ Create** and
    then select **Blank app.**

    <img src="./media/image12.png"
style="width:5.66226in;height:2.20882in" />

2.  Then create on **Create** button in the Blank canvas app and start
    creating Contoso power app.

    <img src="./media/image13.png"
style="width:6.26806in;height:2.62083in" />

3.  In the App name enter **Contoso Product App**, select **Tablet** as
    format and then click on **Create**.

    <img src="./media/image14.png"
style="width:5.51511in;height:2.53759in" />

4.  Welcome to Power Apps Studio window will open click on **Skip**.

    <img src="./media/image15.png"
style="width:6.26806in;height:2.94375in" />

5.  Navigate to **Tree view**, click on three dots on **Screen 1** (…)
    and the select **Rename**. Enter the name as **Product List.**

    <img src="./media/image16.png"
style="width:5.25399in;height:1.82126in" />

6.  In the left-hand navigation pane, go to **Components** under the
    **Tree View.** Click on **+ New Component**.

    <img src="./media/image17.png" style="width:4.25833in;height:2.1in" />

7.  Rename the component to **HeaderLabel** by clicking on the “…” and
    selecting **Rename**.

    <img src="./media/image18.png"
style="width:5.14167in;height:3.63333in" />

    > **Note:** If the **Properties** window does not appear on the right
side, you can easily access it by clicking on the **Properties**
button located in the top bar. This action will open the
**Properties** window, allowing you to view and modify the relevant
settings.

    <img src="./media/image19.png"
style="width:6.26806in;height:0.48333in" />

8.  In the right-hand pane under **Properties**, set the **Width** to
    1400 and **Height** to 100.

    <img src="./media/image20.png"
style="width:2.00833in;height:2.03333in" />

9.  On the Canvas, click **Add an item from the Insert Pane**. From the
    Insert Pane, select **Text Label**.

    <img src="./media/image21.png" style="width:5.43333in;height:2.375in" />

10. In the right-hand pane, under **Properties**, set the following:

    1.  **Text**: Contoso Products

    2.  **Font Size**: 30

    3.  **Text Alignment**: Center

    4.  **Position**: X – 0, Y – 0

    5.  **Width**: 1400, **Height**: 100

    6.  **Text Colour**: White

    7.  **Fill Colour**: blue

    <img src="./media/image22.png"
style="width:1.83333in;height:3.47151in" />

11. Then go to Tree view and select screen. Click on **Insert** from top
    bar. Search and select **HeaderLabel** to use the new component on
    the screen.

    <img src="./media/image23.png"
style="width:6.26806in;height:2.50903in" />

12. Select **Product** **List** screen and go to **Properties**. Select
    **Fill** and choose colour.

    <img src="./media/image24.png"
style="width:6.26806in;height:2.61667in" />

13. Go to **Insert** from top bar and search and select **Text Input**.

    <img src="./media/image25.png"
style="width:6.26806in;height:2.62222in" />

14. Rename the **Text Input** as **SearchBar** and Adjust the location
    and size of Text Input as show in Image.

    <img src="./media/image26.png"
style="width:6.26806in;height:2.77431in" />

15. Go to **SearchBar** input text and then go to **Properties** set the
    default value of search bar as **Notebook.** With the help of this
    bar user can search product by **Category**.

    <img src="./media/image27.png"
style="width:6.26806in;height:1.56111in" />

### Task 2: Add SAP OData Connection in App

1.  Go to Data and select Add data.

    <img src="./media/image28.png"
style="width:6.26806in;height:1.96389in" />

2.  In the Search bar of Add data search for SAP OData and then select
    OData Connection.

    <img src="./media/image29.png"
style="width:6.26806in;height:2.14687in" />

3.  After selecting connection, select Contoso-Product SAP OData
    Connection. Then Connection will be added into the app.

    <img src="./media/image30.png"
style="width:2.84896in;height:1.47544in" />

4.  Choose the table **ProductSet** from the right hand side Choose a
    table section and then select **Connect.**

    <img src="./media/image31.png"
style="width:3.83056in;height:2.65347in" />

5.  Then go to **Insert** and search and select **Vertical Gallery**.

    <img src="./media/image32.png"
style="width:3.55556in;height:2.19306in" />

6.  Select the **ProductSet** as the data source into the vertical
    gallery.

    <img src="./media/image33.png"
style="width:6.26806in;height:2.0875in" />

### Task 3: Configure Product Gallery Screen

1.  Rename the gallery name as **Product Gallery** and adjust the
    gallery as on the canvas as shown in image.

    <img src="./media/image34.png"
style="width:6.26806in;height:1.56667in" />

2.  Click on the **Product Gallery** and go to **Properties** of it,
    configure the layout as Title, Subtitle, Body.

    <img src="./media/image35.png"
style="width:6.26806in;height:1.59306in" />

3.  Go to Product Gallery, By clicking on (…) of each rename **Body** as
    **ProdDescription**, **Subtitle** as **ProdPrice** **and Title** as
    **ProdName.**

    <img src="./media/image36.png"
style="width:4.54206in;height:2.97526in" />

4.  Go to **properties** of Product Gallery and click on 7 Selected,
    configure the selection as per given below:

    | ProdDescription | Description |
    |-----------------|-------------|
    | ProdName        | Name        |
    | ProdPrice       | Price       |

    <img src="./media/image37.png"
style="width:6.26806in;height:1.6625in" />

5.  Go to **Product Gallery** and click on **ProdName**, enter the given
    below formula in the **Text Formula Bar**.

    >  "Product Name :" & ThisItem.Name

    <img src="./media/image38.png" style="width:6.26806in;height:0.7in" />

6.  As same as **ProdName** change the formula of **ProdPrice** and
    **ProdDescription** as given below.

    | ProdPrice       | "Price  :   " & Text(Value(ThisItem.Price),"\$#,###.##") |
    |-----------------|----------------------------------------------------------|
    | ProdDescription | "Description : " & ThisItem.Description                  |

    <img src="./media/image39.png"
style="width:6.26806in;height:0.6625in" />

    <img src="./media/image40.png"
style="width:6.26806in;height:0.57778in" />

7.  Select the **Product Gallery** and Click on **arrow** sign on in the
    gallery canvas. Press **delete** button to remove the arrow.

    <img src="./media/image41.png"
style="width:4.82535in;height:3.21178in" />

8.  Click on the **Product Gallery** and go to formula bar of the
    gallery enter the below given Item formula in the field.

    > Filter(ProductSet,StartsWith(Category,SearchBar.Text))

    <img src="./media/image42.png"
style="width:6.26806in;height:1.43194in" />

9.  Select **Product gallery** then click on the **Pencil** icon on the
    gallery canvas. Then go **Insert** and search and select **Button**.

    <img src="./media/image43.png"
style="width:6.26806in;height:2.05486in" />

    <img src="./media/image44.png"
style="width:6.26806in;height:2.03194in" />

10. Place the button at appropriate position with the help of drag and
    drop. And in the button **Properties** **Text** field enter **Add to
    cart**.

    <img src="./media/image45.png"
style="width:6.26806in;height:1.99028in" />

11. Go to Product gallery click on (…) on the button and rename the
    button as **CartButton**.

    <img src="./media/image46.png"
style="width:6.1672in;height:4.85875in" />

12. Click on the **Add to cart** button and go to formula bar, Select
    **Onselect** and add **formula** as given below.

    > Collect(Collection,{Name:ThisItem.Name,Price:ThisItem.Price,Describe:ThisItem.Description})

    <img src="./media/image47.png"
style="width:6.26806in;height:1.98056in" />

13. Select **Product Gallery** and then go to **Insert** Seach and
    select a **Button**.

    <img src="./media/image48.png" style="width:2.6in;height:2.62986in" />

14. Rename the button as **Reload**. Place the Button at appropriate
    position and set the properties as given below

    | Text        | Reload |
    |-------------|--------|
    | Text Colour | Blue   |
    | Fill Colour | White  |

    <img src="./media/image49.png"
style="width:6.26806in;height:2.65694in" />

15. Click on **Reload** button and Select **OnSelect** and add the below
    given formula into the formula bar.

    > Reset(*SearchBar*)

    <img src="./media/image50.png"
style="width:6.26806in;height:2.61597in" />

### Task 4: Create and Add the Power Apps Table

1.  Go to **Data** section, click on **+ Add Data** and then select
    **Create new tables**. Power Apps tables with open.

    <img src="./media/image51.png"
style="width:3.53333in;height:3.29861in" />

2.  Select **Start from blank** and start creating table.

    <img src="./media/image52.png"
style="width:6.26806in;height:2.3125in" />

3.  By clicking on the table name Rename the tables as **Cart**.

    <img src="./media/image53.png"
style="width:6.26806in;height:2.44861in" />

4.  Click on the down arrow sign of the first column and then select the
    Edit column option. Rename the Display name as **Product Name**.
    Then click on the update button.

    <img src="./media/image54.png" style="width:6.26806in;height:3.175in" />

5.  Select **+ New column** and enter the display name as **Product
    Price**, after entering the name click on **Save**.

    <img src="./media/image55.png"
style="width:4.73681in;height:2.90139in" />

6.  Select **+ New column** and enter the display name as **Customer
    Name**, After entering the name click on **Save**.

    <img src="./media/image56.png"
style="width:5.46076in;height:2.60417in" />

7.  Select **+ New column** and enter the display name as **Customer
    Address**, After entering the name click on **Save**.

    <img src="./media/image57.png" style="width:5.17951in;height:2.875in" />

8.  Select **+ New column** and enter the display name as **Customer
    Contact**, After entering the name click on **Save**.

    <img src="./media/image58.png"
style="width:6.26806in;height:2.14444in" />

9.  From top of the window and click on the **Save and exit**.
    Confirmation windows pop up **again click on Save and exit** to save
    the table. It will automatically redirect to Contoso app.

    <img src="./media/image59.png"
style="width:6.26806in;height:2.85139in" />

### Task 5: Create Order Summary Screen form Contoso Product App

1.  Go to **Tree** **view** 🡪 **Screens**. Click on **+ New Screen** and
    then select **Blank.**

    <img src="./media/image60.png"
style="width:2.71111in;height:2.65278in" />

2.  Go to **Screen 2**. Click on (…) three dots and select **Rename**.
    Rename the screen 2 as **Order Summary**.

    <img src="./media/image61.png"
style="width:6.26806in;height:2.63194in" />

3.  Select **Order Summary**, go to **Insert** then search and select
    **HeaderLabel.**

    <img src="./media/image62.png"
style="width:6.26806in;height:2.65556in" />

4.  Select **Order Screen**, go to **Insert** then search and select
    Vertical Gallery**.**

    <img src="./media/image63.png" style="width:2.85in;height:2.85972in" />

5.  Go to **Gallery**, click on three dots next to gallery name. select
    **Rename** and rename the gallery as **OrderGallery**. Place the
    **OrderGalley** at appropriate position as shown in **image**. Go to
    the **formula bar** of the **OrderGallery** select **Items** and
    enter the below given **formula**.

    > Collection

    <img src="./media/image64.png"
style="width:6.26806in;height:2.02153in" />

6.  Click on the **OrderGallery**, go to properties and change the
    Layout as **Title, subtitle, body.**

    <img src="./media/image65.png" style="width:6.26806in;height:1.7in" />

7.  Click **on Order Summary** Screen, got to properties. Change the
    **colour** **fill** same as the previous screen.

    <img src="./media/image66.png" style="width:6.26806in;height:1.7in" />

8.  Go to **Product List** screen and go to **Insert**. Search and
    select the **Button**.

    <img src="./media/image67.png"
style="width:3.62778in;height:3.18403in" />

9.  Go to **Button**, click on three dots and select **Rename**.
    **Rename** the button as **MyCart**.

    <img src="./media/image68.png"
style="width:6.26806in;height:2.16944in" />

10. Select **MyCart** button, place the button at appropriate place and
    then go to properties. Set the properties of the button as given
    below.

    | Text        | Go to Cart |
    |-------------|------------|
    | Text colour | Blue       |
    | Fill Colour | White      |

    <img src="./media/image69.png"
style="width:6.26806in;height:2.87569in" />

11. Click on the **MyCart** button and enter the below given formula in
    formula bar as **OnSelect**.

    > Navigate(*'Order Summary'*)

    <img src="./media/image70.png"
style="width:6.26806in;height:2.67222in" />

12. Click on the **Order Summary**, Go to Insert, search and select
    **Button**.

    <img src="./media/image71.png" style="width:3.65in;height:3.19444in" />

13. **Rename** the button as **Back** and place it at appropriate place.
    Change the **properties** of button as given below.

    | Text        | Back  |
    |-------------|-------|
    | Text Colour | Blue  |
    | Fill Colour | White |

    <img src="./media/image72.png"
style="width:6.26806in;height:2.65278in" />

14. Select **Back** button and enter the below given formula as
    **OnSelect**.

    > Navigate(*'Product List'*)

    <img src="./media/image73.png"
style="width:6.26806in;height:2.19028in" />

15. Click on **OrderGallery** and go to properties of the gallery. Click
    on the 7 selected option and select the fields as given below.

    <img src="./media/image74.png"
style="width:6.26806in;height:2.29097in" />

16. Go to **OrderGallery,** select Body and rename the body as
    **CartProDes**. Then Enter the given below **formula** in formula
    bar as Text.

    > "Description  :  " & ThisItem.Describe

    <img src="./media/image75.png"
style="width:6.26806in;height:1.30069in" />

17. Repeat the process for **Subtitle** of **OrderGallery**, rename as
    **CartProdPrice** and enter the **formula** as given below.

    > "Price  :   " & Text(Value(ThisItem.Price),"\$#,###.##")

    <img src="./media/image76.png"
style="width:6.26806in;height:1.03333in" />

18. Repeat the same process for **Title**, rename as **CartProdName**
    and enter the **formula** as given below.

    > "Product Name :  " & ThisItem.Name

    <img src="./media/image77.png"
style="width:6.26806in;height:1.26111in" />

19. Select **OrderGallery**, click on the **pencil** icon in the gallery
    canvas field, go to **Insert**. Search and select **Cancel** Icon.

    <img src="./media/image78.png"
style="width:6.26806in;height:2.13472in" />

    <img src="./media/image79.png"
style="width:3.88333in;height:2.53958in" />

20. Select and place the **Cancel** Icon at appropriate place as shown
    in image. Enter the formula given below as **OnSelect**.

    > Remove(Collection,ThisItem)

    <img src="./media/image80.png"
style="width:6.26806in;height:2.40486in" />


### Task 6: Add Customer Information section

1.  Click on **Order Summary**, Go to Insert. Search and Select **Text
    Label**.

    <img src="./media/image81.png"
style="width:6.26806in;height:2.85347in" />

2.  Repeat the previous step for two more times and place the **Text
    label** at the appropriate place as show in image.

    <img src="./media/image82.png"
style="width:6.26806in;height:3.19444in" />

3.  Double click on each label one by one and enter the text as **Full
    Name, Phone Number, Address**. The final output show as given below
    image. Readjust the label if required.

    <img src="./media/image83.png"
style="width:6.26806in;height:3.03611in" />

4.  Select **Order Summary**, go to Insert. Search and select for **Text
    Input.**

    <img src="./media/image84.png" style="width:2.75in;height:2.65208in" />

5.  Rename the Input Text as **NameInput** and Place the Input Text just
    below the **Full Name**. Go to **properties** of the **NameInput**
    and Remove **Text** (Text Input) from **Default**

    <img src="./media/image85.png" style="width:6.26806in;height:1.975in" />

6.  Repeat the process select the **Text Label** Rename as
    **PhoneInput** and place at below the **Phone Number**. From
    properties remove **Default** text.

    <img src="./media/image86.png"
style="width:6.26806in;height:1.96806in" />

7.  Repeat the process select the **Text Label** Rename as
    **AddressInput** and place at below the Address. From properties
    remove **Default** text.

    <img src="./media/image87.png"
style="width:6.26806in;height:1.97014in" />

8.  Select **Order Summary**, go to **Insert**. Search and Select a
    **Button**.

    <img src="./media/image88.png"
style="width:2.67222in;height:2.84792in" />

9.  Click on the button and then select (…) and rename it as **Submit.**
    Place the **Submit** button just below the **AddressInput**. Go to
    **Properties** of the **Submit** button, In the **Text** enter
    **Submit** as Text.

    <img src="./media/image89.png"
style="width:6.26806in;height:1.95764in" />

10. Select the submit button, enter the given below formula as OnSelect.

    > Patch(Carts,Defaults(Carts),{'Product Name':*CartProdName*.Text,'Product
Price':*CartProdPrice*.Text,'Customer Name':*NameInput*.Text,'Customer
Contact':*PhoneInput*.Text,'Customer Address':*AddressInput*.Text})

    <img src="./media/image90.png"
style="width:6.26806in;height:2.38819in" />

11. Click on the **Save** button from the right side of the top bar to
    **Save** the app.

    <img src="./media/image91.png"
style="width:6.26806in;height:2.38819in" />

## Exercise 3: Test Contoso Product App

1.  From the top bar click on the Play button to start testing.

    <img src="./media/image92.png"
style="width:6.26806in;height:0.70069in" />

2.  Search **Camcorder** In the search field, and then click on the
    **Add to cart** Button.

    <img src="./media/image93.png"
style="width:6.26806in;height:3.07222in" />

3.  Search **Notebook** in the search field and choose a notebook and
    click on the **Add to cart** button. After that click on **Go to
    Cart** Button.

    <img src="./media/image94.png"
style="width:6.26806in;height:3.19028in" />

4.  Enter the Full Name Phone Number and Address and then click on
    submit. The order is placed for the products.

    <img src="./media/image95.png"
style="width:6.26806in;height:2.77708in" />

5.  Go to Power apps Tables and check the order Entry.

    <img src="./media/image96.png"
style="width:6.26806in;height:1.07292in" />

### Conclusion

In this lab, participants learned how to create an SAP OData connection within Power Apps, design a custom app (Contoso Product App), and integrate it with SAP data. They practiced adding SAP OData data to the app, configuring a product gallery to display items, and building functionality to filter, search, and add items to a cart. Additionally, participants created an order summary screen, added customer information input fields, and implemented a submission process using Power Apps tables. Finally, they tested the app by searching and adding products to the cart, enhancing their skills in Power Apps and SAP integration.

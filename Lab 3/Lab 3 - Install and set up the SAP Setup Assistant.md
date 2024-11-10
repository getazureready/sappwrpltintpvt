# Lab 3 Install and set up the SAP Setup Assistant

## Objective: 

This lab is designed to guide participants through the
process of setting up and configuring the SAP Setup Assistant within the
Microsoft Power Platform environment. Participants will learn how to
establish necessary connections, install the SAP Setup Assistant, update
connection references, enable cloud flows, and access the SAP Setup
Assistant canvas app. This lab provides a hands-on approach to preparing
the Power Platform environment for integration with SAP, enabling
participants to connect to various services and configure essential
settings.

## Solution Foucs Area

This lab focuses on setting up the SAP Setup Assistant in Power Platform. It covers creating connections to essential services, installing the app, updating connection references, enabling cloud flows, and using the canvas app to streamline SAP integration processes.

**Estimated Time:** 20 mins

## Task 1: Create Connection

1.  Navigate to
    +++https://www.microsoft.com/en-in/power-platform/products/power-apps+++
    and sign in with Admin tenant ID. From the top bar in Power apps select the **Dev One** environment.

    ![](./media/image5.png)


2.  From the left navigation bar click on **More** and select
    **Connections.**

    ![](./media/image6.png)


3.  From the top bar click on the **+ New Connection.**

    ![](./media/image7.png)


4.  In the top right search bar, search for +++**Microsoft Dataverse**+++ and
    then select **Microsoft Dataverse**.

    ![](./media/image8.png)


5.  Click on the **Create**, to create the connection.

    ![](./media/image9.png)

6. Then Pick an account window will pop up, select the admin tenant
    account to complete the connection.

    ![](./media/image10.png)


7. Repeat the same process to create the below given connections.

    - **Office 365 Outlook**

    - **Office 365 Users connector**

    - **Power Apps for Makers connector**

    - **Power Automate Management**

    - **Power Platform for Admins connector**

    - **Power Query Dataflows connector**

    ![](./media/image11.png)


## Task 2: Install SAP Setup Assistant from AppSource

1.  Navigate to
    +++https://appsource.microsoft.com/en-us/product/dynamics-365/powerplatformtemplates.mpa_sapsetupassistant+++
    and click on the **Get it now**.

    ![](./media/image12.png)

2.  The Power platform admin center will open, select the **Dev One**
    Environment, select both the check box and click on **Install**.
    This process install **SAP Setup Assistance** in the Dev One
    Environment.

    ![](./media/image13.png)


3.  After Installation go to environment 🡪 Dev One 🡪 Dynamic 365 Page
    and confirm the installation status.

    ![](./media/image14.png)


## Task 3: Update Connection Reference

1.  Navigate to Power apps, From the left navigation bar select
    **Solutions** and open **Default Solution.**

    ![](./media/image15.png)


2.  Select **Connection References** from the list of the Objects in the
    left pane and then select and open **SAP Setup Assistant –
    Dataverse**.

    ![](./media/image16.png)


3.  In Edit SAP Setup Assistant – Dataverse tab, click on the
    **Connection** dropdown and the select **Admin Tenant Id**, in which
    we create the connection. After that click on the **Save** button
    and again click on **Save Changes**.

    ![](./media/image17.png)


4.  Repeat the Same process for the below given connections:

    - **SAP Setup Assistant - Office 365 Outlook**

    - **SAP Setup Assistant - Office 365 Users**

    - **SAP Setup Assistant - Power Apps for Makers**

    - **SAP Setup Assistant - Power Automate Management**

    - **SAP Setup Assistant - Power Platform for Admins**

    - **SAP Setup Assistant - Power Query Dataflows**

## Task 4: Turn on Cloud Flow

1.  From the left navigation pane click on **Solution**, then click on
    **Manged** and select and open **SAP Setup Assistant**.

    ![](./media/image18.png)


2.  From the left navigation pane, select **Cloud Flows**. Locate any
    flows showing an **Off** status and turn them **On**.

    ![](./media/image19.png)


## Task 5: Use the SAP Setup Assistant

You are now ready to use the **SAP Setup Assistant** canvas app,
installed as part of the SAP Setup Assistant solution.

**Conclusion:**

By the end of this lab, participants will have gained practical skills
in creating and configuring essential connections within Power Platform.
They will learn how to install applications from Microsoft AppSource,
manage connection references, and activate cloud flows, which are
critical components for seamless SAP integration. Additionally,
participants will be able to navigate the Power Platform environment
confidently, applying this knowledge to streamline data connectivity and
enhance automation capabilities with SAP systems.

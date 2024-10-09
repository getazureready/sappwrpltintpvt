# Setting up Lab Environment

<table>
<colgroup>
<col style="width: 21%" />
<col style="width: 78%" />
</colgroup>
<thead>
<tr>
<th>Objective </th>
<th><p>In this lab, participants will take on the role of an IT
Administrator at <strong>Contoso</strong>, tasked with enabling
collaboration and app development for a project team. You'll assign a
Power Apps trial license to a new developer, setting up a development
environment, and create a dedicated Microsoft Teams space, complete with
channels, for seamless project communication and collaboration. This
hands-on lab will help you understand how to provision access to Power
Apps and manage team collaboration in Teams effectively.</p>
<p> </p></th>
</tr>
</thead>
<tbody>
<tr>
<td>Prerequisites </td>
<td><p>To complete this lab, you need a Microsoft 365 admin tenant, a
Power Apps trial license, a Microsoft Teams trial license, and access to
the Power Platform admin center. Ensure all necessary licenses and
access permissions are in place before starting.</p>
<p> </p></td>
</tr>
<tr>
<td>Duration </td>
<td>30 mins </td>
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


# Task 1: Assign Power Apps trial license

- Open a web browser and go to
  <https://powerapps.microsoft.com/en-us/free/>.

  <img src="./media/image1.png"
style="width:6.26806in;height:3.27466in" />

- Select **Start free**.

  <img src="./media/image2.png" style="width:6.26806in;height:3.38582in"
alt="A person with his arms crossed Description automatically generated" />

- Enter your **Office 365 admin credential**, check the checkbox to
  **accept the agreement** and click on **Start your free trial.**

  <img src="./media/image3.png" style="width:6.26806in;height:3.54252in"
alt="A screenshot of a computer Description automatically generated" />

- Enter **password of your** **Office 365 tenant Id** and then select
  **Sign in.**

  <img src="./media/image4.png" style="width:6.26806in;height:4.61598in"
alt="A login box with a blue box and red box with black text Description automatically generated" />

- Select **Yes** on **Stay signed in?** pop-up window.

  <img src="./media/image5.png" style="width:6.26806in;height:4.79645in"
alt="A screenshot of a computer error Description automatically generated" />

- Provide **Contact Information** as below and then select **Submit.**

  - **Email:** Office 365 admin tenant credentials

  - **Country/region**: United States

  - **Phone number**: Your phone number

  <img src="./media/image6.png" style="width:6.26806in;height:3.65045in"
alt="A screenshot of a computer screen Description automatically generated" />

- You can now see **Home page of Power Apps**. From the environment
  selector, select the developer environment – **Dev One** which is
  created for you.

  <img src="./media/image7.png" style="width:6.26806in;height:3.68105in"
alt="A screenshot of a computer Description automatically generated" />

- Open the new tab and go to Power Platform admin center by navigating
  to <https://admin.powerplatform.microsoft.com> and if required, sign
  in using your given Office 365 tenant admin credentials. **Close**
  **the Pop-up window** saying, ‘Welcome to the Power Platform admin
  center’.

  <img src="./media/image8.png"
style="width:6.26806in;height:3.65045in" />

- From the left navigation pane, select **Environments** and then you
  can see, **Dev One** is your Dataverse environment.

  <img src="./media/image9.png" style="width:6.26806in;height:3.69606in"
alt="A screenshot of a computer Description automatically generated" />

# Task 2: Create a team in Microsoft Teams 

- Sign in to Microsoft Teams using <https://teams.microsoft.com/> with
  your Office 365 tenant credentials.

- Close the pop-up window.

  <img src="./media/image10.png" style="width:6.26806in;height:3.90682in"
alt="A screenshot of a computer screen Description automatically generated" />

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr>
<th><p><strong>Note:</strong> If pop-up asks you to switch to the new
Teams, select Switch now and follow the below instructions a and b.</p>
<ul>
<li><p>window, select <strong>Get Started.</strong></p></li>
</ul>
<p><img src="./media/image11.png"
style="width:4.74025in;height:3.92138in"
alt="A screenshot of a phone Description automatically generated" /></p>
<ul>
<li><p>Close the window which is asking for scanning QR code.</p></li>
</ul>
<p><img src="./media/image12.png"
style="width:5.53545in;height:3.3496in"
alt="A qr code on a white background Description automatically generated" /></p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

- In the Sidebar on the left, click **Teams**, click on **+ icon** to
  join or create a team.

  <img src="./media/image13.png" style="width:6.26806in;height:3.52662in"
alt="A screenshot of a computer Description automatically generated" />

- Click on **Create team.**

  <img src="./media/image14.png" style="width:4.8861in;height:4.64648in"
alt="A screenshot of a team Description automatically generated" />

- For old Teams, select **From a scratch**. If you have switched to new
  Teams, follow the below steps a, b and c and directly go to the step
  8.

  <img src="./media/image15.png" style="width:6.26806in;height:6.4453in"
alt="A screenshot of a team Description automatically generated with medium confidence" />

- Enter the Team name – Test Team. Click on Private.

  <img src="./media/image16.jpeg" style="width:6.26806in;height:3.28327in"
alt="A screenshot of a computer Description automatically generated" />

- Select Org-wide.

  <img src="./media/image17.jpeg" style="width:6.26806in;height:3.53556in"
alt="A screenshot of a computer Description automatically generated" />

- Select **Create** and go to step 8 directly.

  <img src="./media/image18.jpeg" style="width:6.26806in;height:5.99902in"
alt="A screenshot of a computer Description automatically generated" />

- Select **Org-wide** for What kind of team this will be?

  <img src="./media/image19.png" style="width:3.74125in;height:3.85197in"
alt="A screenshot of a computer Description automatically generated with medium confidence" />

- Give a **Name** to your team as **Test Team** and click **Create.**

  <img src="./media/image20.png" style="width:6.26806in;height:6.59829in"
alt="A screenshot of a computer Description automatically generated" />

- To create a channel within this team, select the team **Test Team**
  that you created, click **More options … \\ Add channel.**

  <img src="./media/image21.png" style="width:4.8861in;height:8.19906in"
alt="A screenshot of a computer Description automatically generated" />

- Give a name to the Channel as **"TestChannel",** select the channel
  type as **Standard** and then click **Add/Create.**

  <img src="./media/image22.png" style="width:6.26806in;height:4.66597in"
alt="A screenshot of a channel Description automatically generated" />

- You can view the channel in teams when added.

  <img src="./media/image23.png" style="width:4.85484in;height:4.75066in"
alt="A screenshot of a computer Description automatically generated" />

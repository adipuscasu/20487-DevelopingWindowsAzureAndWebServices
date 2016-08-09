# Module 1: Overview of Service and Cloud Technologies

# Lesson 4: Cloud Computing

### Demonstration: Exploring the Microsoft Azure portal

#### Demonstration Steps

1. On the **Start** screen, click the **Internet Explorer** tile.
2. In Internet Explorer, go to **https://manage.windowsazure.com**.
3. If a page appears, prompting for your email address, type your email address, and then click **Continue**. Wait for the **Sign In** page to appear, type your email address and password, and then click **Sign In**.

   >**Note** : During the sign-in process, if a page appears prompting you to choose from a list of previously used accounts, select the account that you previously used, and then continue to provide your credentials.

4. Review the items in the pane on the left side of the screen and explain the different services that you can manage with the Azure portal.
5. Click **NEW** on the lower-left corner of the portal. Click **COMPUTE** , click **CLOUD SERVICE** , and then click **QUICK CREATE**. The **URL** and **REGION** text boxes display on the right side of the screen.
6. In the **URL** text box, type the following cloud service name: **CloudServiceDemo YourInitials** (Replace **YourInitials** with your initials).
7. Explain that the cloud service name you typed is going to be part of the URL that you will use when connecting to the roles running in the cloud service.
8. In the **REGION** drop-down list, select the region that is closest to your location.  
Explain that by selecting the region, you are actually selecting the datacenter where the VMs will be created.

9. Click **CREATE CLOUD SERVICE** at the lower-right corner of the portal. Wait until the cloud service is created.
10. Click **CLOUD SERVICES** in the navigation pane.
11. Click the cloud service that you created in the previous step (the one that is named **CloudServiceDemo YourInitials**.
12. Explain that currently the cloud service is empty and has no roles; therefore, the tabs do not have any content. Explain that in module 06, &quot;Hosting Services&quot;, you will show how to deploy new roles to the cloud service, and how to configure the roles.
13. Go over the different tabs and explain their purpose:
  a. **DASHBOARD**. Provides an overview for the state and configuration of the cloud service and its roles.  
  b. **MONITOR**. Shows performance counter metrics for the roles, such as their CPU and memory usage.  
  c. **CONFIGURE**. Allows you to control settings such as monitoring capabilities, remote access, and selection of the guest operating system.  
  d. **SCALE**. Allows you control the number of instances (VMs) used for each role.  
  e. **INSTANCES**. Allows you to control the existing instances (shutdown/start, restart, and remote desktop).  
  f. **LINKED RESOURCES**. Allows you to manage the list of dependent resources, such as storage and databases. By linking to resources, you can monitor and control the scale of all the resources from the cloud service configuration.  
  g. **CERTIFICATES**. Allows you to manage the certificates used by the roles, for example for HTTPS communication.  
14. Close Internet Explorer.

# Lesson 5: Exploring the Blue Yonder Airlines&#39; Travel Companion Application

### Demonstration: Using the Travel Companion Application

#### Demonstration Steps

1. In the virtual machine **20487B-SEA-DEV-A** , on the **Start** screen, click the **Computer** tile to open File Explorer.
2. Go to **D:\AllFiles\Mod01\DemoFiles\BlueYonderDemo\Setup**.
3. Double-click the **SetupIIS.cmd** file and wait for the script to finish.
4. Explain to the students that this script builds the server solutions and deploys them to the local IIS server.
5. In the virtual machine **20487B-SEA-DEV-C** , on the **Start** screen, click the **Visual Studio 2012** tile.
6. On the **File** menu, point to **Open** , and then click **Project/Solution**.
7. Go to **D:\AllFiles\Mod01\DemoFiles\BlueYonderDemo\BlueYonder.Companion.Client** ,select the **BlueYonder.Companion.Client.sln** file, and then click **Open**.
8. If the **Developers License** dialog box displays, click **I Agree**.
9. If the **User Account Control** dialog box displays, click **Yes**.
10. In the **Developers License** dialog box, type your email address and a password, and then click **Sign in**.
11. In the **Developers License** dialog box, click **Close**.

   >**Note** : If you do not have valid email address, click **Sign up** and register for the service.  
   >Write down these credentials and use them whenever you are required to use an email address.

12. In Solution Explorer, right-click the **BlueYonder.Companion.Client** project, and then click **Set as StartUp Project**.
13. Press Ctrl+F5 to start the client app without debugging.
14. If you are prompted to allow the app to run in the background, click **Allow**.
15. Briefly explain the purpose and features of the Blue Yonder Companion app: it is a travel reservation and management app. It can help you search and book flights, manage your trip schedule, store and manage pictures and videos from trips, and provide weather information for your trip destinations.
16. After the client app starts, right-click or swipe from the bottom of the screen to open the app bar.
17. Click **Search** , and then in the **Search** text box, type **New**.
18. If you are prompted to allow the app to share your location, click **Allow**.
19. Explain that the app communicates with the front-end service to retrieve a list of flights to a location whose name begins with _New_, for example, New York.
20. Select any destination from the list of search results, and then click the **Purchase this trip** link.
21. In the **First Name** text box, type your first name.
22. In the **Last Name** text box, type your last name.
23. In the **Passport** text box, type **Aa1234567**.
24. In the **Mobile Phone** text box, type **555-5555555**.
25. In the **Home Address** text box, type **423 Main St.**
26. In the **Email Address** text box, type your email address.
27. Click **Purchase**.
28. Explain that now the app sends the purchase request to the front-end service. The front-end service saves the purchase information and then sends a separate purchase request to the back-end service for additional processing. After the back-end and front-end services complete their task, the client app displays a confirmation message.
29. Inform the students they will implement the purchase feature, including the back-end service purchase feature, in the upcoming labs.
30. Click **Close** to close the confirmation message.
31. On the **Blue Yonder Companion** page, point to **New York at a Glance** , and explain that the weather forecast is also retrieved from the front-end service. Inform the students that they will implement the weather service in the upcoming labs.
32. Click the current trip from Seattle to New York.
33. On the **Current Trip** page, right-click or swipe from the bottom of the screen to display the app bar, and then click **Media**.
34. On the **Media** page, right-click or swipe from the bottom of the screen to display the app bar.
35. Show students the availablebuttons, and explain that you can upload images and videos to Azure Storage, and share them with other clients.
36. Inform the students that they will implement the upload and download features in the upcoming labs.

   >**Note** : Do not click the upload buttons, because you have not created any Azure Storage accounts yet. If you click any of the upload buttons, the app will fail and close.

37. Close the client app.
38. Return to the **20487B-SEA-DEV-A** virtual machine, and then on the **Start** screen, click the **Computer** tile to open File Explorer.
39. Go to **D:\AllFiles\Mod01\DemoFiles\BlueYonderDemo\Setup**.
40. Double-click the **CleanIIS.cmd** file and wait for the script to finish executing.

   >**Note** : The **CleanIIS.cmd** script reverses the changes made to IIS by using the **SetupIIS.cmd** script that you executed at the beginning of this demonstration.
# **Exercise 3: Access the Published Applications and Desktop using Browser**


## **Task 1: Access the Published Application**

In this exercise, we will access the Desktop and RemoteApps assigned to us in the previous exercise using browser.

1. Open the following URL in a new browser tab, this will lead us to the Remote Desktop Web Client.

   ```aka.ms/wvdarmweb``` 

2. Now to login, enter the lab credentials as mentioned below:

   - Username: *Paste your username* **<inject key="AzureAdUserEmail" />** *and then click on **Next**.*
   
   ![ws name.](media/95.png)

   - Password: *Paste the password* **<inject key="AzureAdUserPassword" />** *and click on **Sign in**.*

   ![ws name.](media/96.png)
  
> **Note:** If you see a window popup titled ***Help us protect your account***, select the **Skip for now** option.
>
>    ![](media/login.png)

3. After the Windows Virtual Desktop (WVD) dashboard is launched, click on the **Word** application to access it. 

   ![ws name.](media/ag8.png)


4. Select **Allow** on the prompt asking permission to *Access local resources*.

   ![ws name.](media/128.png)


5. Enter the lab credentials to access the application and click on **Submit**.

   - Username: **<inject key="AzureAdUserEmail" />** 
  
   - Password: **<inject key="AzureAdUserPassword" />**

   ![ws name.](media/89.png)
      
6. The Word application will launch and will look similar to the screenshot below. Click on **Sign in**.

   ![ws name.](media/ch9.png)

7. Enter the username **<inject key="AzureAdUserEmail" />** on *Activate Office* window and click on **Next**.

   ![ws name.](media/ch6.png)

8. Enter the password **<inject key="AzureAdUserPassword" />** and click on **Sign in**.

   ![ws name.](media/ch7.png)
   
> **Note:** If there's a dialog box saying ***Help us protect your account***, then select **Skip for now** option.
>
>    ![](media/login.png)

9. Click on **Close** button on the window asking *Your privacy option*.

   ![ws name.](media/ch19.png)

10. Once signed in, the application will look similar to the screenshot below 

   ![ws name.](media/ch8.png)


## **Task 2: Access the published Desktop**

1. On the top-left side of Remote Desktop Web Client, click on **All Resources**.
   
   ![ws name.](media/w12.png)
   
   
2. You will be redirected to the WVD dashboard. Click on **Default Desktop** to launch it.

   ![ws name.](media/ag9.png)


3. Select **Allow** on the prompt requesting permission to *Access local resources*.

   ![ws name.](media/93.png)


4. Enter the lab credentials to access the application and click on **Submit**.

   - Username: **<inject key="AzureAdUserEmail" />** 
  
   - Password: **<inject key="AzureAdUserPassword" />**

   ![ws name.](media/89.png)


5. The virtual desktop will launch and look similar to the screenshot below. 

   ![ws name.](media/ch12.png)
   
6. Navigate back to the Azure Portal, search for *Windows virtual desktop* in the top search bar and select **Windows Virtual Desktop** from the suggestions.

   ![ws name.](media/w1.png)

7. Click on **Users** under the *Manage* blade, then paste **<inject key="AzureAdUserEmail" />** in the search bar and click on your user to open it.

   ![ws name.](media/jvm7.png)

8. Under the **Sessions** tab, select both the Host pools by clicking on the checkbox and then click on the **Log off** button.

   ![ws name.](media/jvm8.png)

9. Click on **OK** to *Log off user from VMs*.

   ![ws name.](media/jvm9.png)

10. Click on **Refresh** button and make sure *No results* is displayed under Host pool.

   ![ws name.](media/jvm9.png)

11. Click on the **Next** button present in the bottom-right corner of this lab guide. 


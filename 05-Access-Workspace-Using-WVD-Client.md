# **Exercise 4: Access the Published Applications and Desktop using WVD Desktop Client**

In this exercise, we will access the Desktop and RemoteApps assigned to us in the previous exercise using Windows Virtual Desktop (WVD Desktop client.

## **Task 1: Access the Published Applications**

1. Open the following URL in a new browser tab.

   ```https://docs.microsoft.com/en-us/azure/virtual-desktop/connect-windows-7-10#install-the-windows-desktop-client```

> **Note:** To download *WVD Mac Client* on **macOS**, use the link given below:
>
> ```https://docs.microsoft.com/en-us/azure/virtual-desktop/connect-macos```

2. Under *Install the Windows Desktop Client*, click on **Windows 64-bit**. This will download the **WVD Desktop Client** on your local machine.
   
   ![ws name.](media/a48.png)
      
3. After the download completes, open the setup to run it. Then on the Welcome page of setup click on **Next**.

4. Check the agreement box and click on **Next**.

5. Under the **Installation scope** section select **Install just for you** and then click on **Install**.

   ![ws name.](media/wvd41.png)

6. After the installation completes successfully, Click on the **Start** icon using your local machine and search for **Remote desktop**. Open the remote desktop application with exact icon as shown below.

   ![ws name.](media/137.png)
   
   
7. Once the **Remote Desktop** application opens, click on **Subscribe**.

   ![ws name.](media/a49.png)
  
  
8. Enter your **credentials** to access the workspace.

   - Username: *Paste your username* **<inject key="AzureAdUserEmail" />** *and then click on **Next**.*
   
   ![ws name.](media/95.png)

   - Password: *Paste the password* **<inject key="AzureAdUserPassword" />** *and click on **Sign in**.*

   ![ws name.](media/96.png)

> **Note:** If you see a window popup stating ***Help us protect your account***, select **Skip for now** option.
>
>    ![](media/login.png)
   
9. Make sure to **uncheck** *Allow my organization to manage my device* and click on **OK**.

   ![ws name.](media/jvm5.png)
   
   
10. After the WVD dashboard launches, double click on the **Excel** application to access it.

   ![ws name.](media/ag10.png)
   

11. A window saying *Starting your app*, will appear. Wait for few seconds, then enter your password to access the Application.

   - Password: **<inject key="AzureAdUserPassword" />**
   
   ![ws name.](media/ch14.png)
   
12. Wait for the Application to connect.

   ![ws name.](media/58.png)
   

13. The Excel application will launch and will look similar to the screenshot below.

   ![ws name.](media/ch15.png) 
    
14. You can exit from the window of Excel Application by clicking on the **X icon**.

   ![ws name.](media/ch16.png)
   
## **Task 2: Access the Virtual Desktop**


1. Click on the **Start** icon using your local machine and search for **Remote desktop** and open the remote desktop application with icon identical to the one shown below.

   ![ws name.](media/51.png)
 
2. The WVD client application will launch and you will be redirected to the WVD dashboard. Click on named **Default Desktop** to launch the desktop.

   ![ws name.](media/ag11.png)
   

3. A window saying *Connecting to: Default Desktop* will appear. Wait for few seconds, then enter your password and click **Ok** to access the Desktop.

   - Password: **<inject key="AzureAdUserPassword" />**
   
   ![ws name.](media/ch14.png)
   

4. Wait for the Default Desktop to connect.

   ![ws name.](media/ch17.png)
   

5. Your virtual desktop will launch and look similar to the screenshot below. You can exit from the window by clicking on **X icon***. 
        
   ![ws name.](media/jvm22.png)  
    
     
6. Click on the **Next** button present in the bottom-right corner of this lab guide. 

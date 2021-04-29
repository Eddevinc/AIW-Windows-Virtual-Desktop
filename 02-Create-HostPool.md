# **Exercise 1: Create Host Pool from Azure Portal** 

 
A Host Pool is a collection of Azure virtual machines that register to Windows Virtual Desktop as session hosts when you run the Windows Virtual Desktop agent. All session host virtual machines in a host pool should be sourced from the same image for a consistent user experience. To start with, we will login to the Azure portal. 
 
 
### **Task 1: Log in to Azure Portal**

>**Note:** It is important that you login to the cloud environment using **Incognito window** only.

1. Open **Azure Portal** (https://portal.azure.com) in your browser. 

2. Login to Azure with the username **<inject key="AzureAdUserEmail" />** and click on **Next**.

   ![](media/w24.png)

3. Enter the password **<inject key="AzureAdUserPassword" />** and click on **Sign in**.

   ![](media/w25.png)

> **Note:** If there's a dialog box saying ***Help us protect your account***, then select the **Skip for now** option.
>
>    ![](media/login.png)
>
> **Note:** First time users may get a prompt to **Stay signed in**, click on **No**.
>
>    ![](media/w26.png)
>   
> **Note:** If you see a _**Welcome to Microsoft Azure**_ popup window offering you an introductory **Start Tour** option, select **Maybe later** to skip.
>
>    ![](media/wvd4.png) 
 
### **Task 2: Create Host Pool**

In this exercise, we will create a Host Pool named *WVD-HP-01* of pooled type, then add two session hosts (virtual machines) i.e. *WVD-HP01-SH-0* and *WVD-HP01-SH-1*  and register the default desktop application group from this hostpool to a new workspace named *WVD-WS-01*.

1. On the **Azure portal** search for *Windows Virtual Desktop* in the top search bar and select **Windows Virtual Desktop** from the suggestions.

   ![ws name.](media/w1.png)
 

2. You will get directed to the Windows Virtual Desktop (here after referred to as WVD) management window.  

   ![ws name.](media/64.png)

3. Now select **Host pools** under the **Manage** blade and click on **+ Add** to add new Host Pool.

   ![ws name.](media/z.png)

4. In this step, we will provide the details required to create a Host Pool. For your convenience, this step is divided into two sections:

 **A.** **Project Details –** Defines the Host Pool environment 

   - Subscription: *Choose the default subscription*.
   - Resource Group: *Select **WVD-RG** from the drop down*.
   - Host Pool Name: **WVD-HP-01**
   - Location: **East US**, *basically this should be same as the region of your resource group*.      
   - Validation environmet: **No**
      
   >**Note:** Validation host pools let you monitor service updates before rolling them out to your production environment.
            
   ![ws name.](media/w9.png)
   
 **B.** **Host Pool Type –** Defines the type of host pool. 

   - Host pool type: **Pooled** 
   
      
   >**Note:** Host Pools are of 2 types: Pooled and Personal.  
   > - **Pooled:** where session hosts can accept connections from any user authorized to an app group within the host pool.
   > - **Personal:**, where each session host is assigned to individual users.

   - Max session limit: **5**
   
      
   >**Note:** Max session limit helps to regulate the number of simultaneous users on the same session host.
     
   - Load Balancing Algorithm: **Breadth First**
   
      
   >**Note:** Load Balancing Algorithm is of two types: *Breadth-first* and *Depth-first*. 
   >    - **Breadth-first** load balancing allows you to evenly distribute user sessions across the session hosts in a host pool. 
   >    - **Depth-first** load balancing allows you to saturate a session host with user sessions in a host pool. 
     
   - Click on **Next:Virtual Machines**.
   
   ![ws name.](media/w10.png)  
   
5. In the Virtual machines tab, select **Yes** to **Add virtual machines**. By doing this, we are stepping towards adding Virtual machines to the host pool. 

   ![ws name.](media/66.png)

6. In this step, we will provide the details of the VMs to be created as session Hosts. For your convenience, this step is divided into three sections as follows:

  **A**. Session Host Specifications:     

   - Resource Group: *Select **WVD-RG** from the drop down*.
   - Virtual machine location: **East US**, *location should be same as the location of your resource group*.
   - Virtual machine size: **Standard D4s_v3**. *Click on **Change Size**, then select **D4s_v3** and click on **Select** as shown below*
   
   ![ws name.](media/ch1.png)

   - Number of VMs: **2**   
   - Name prefix: **WVD-HP01-SH** 
   - Image type: **Gallery**
   - Image: **Windows 10 Enterprise multi-session, version 1909 + Microsoft 365 Apps** *(choose from dropdown)* 
   - OS disk type: **Standard SSD**
   - Use managed disks: *Leave to default*
   
   ![ws name.](media/ch3.png)
    
  **B**. Network and Security:
    
   Leave all values to default, except:
    
   - Virtual network: **aadds-vnet** *(choose from dropdown)*
   - Subnet: **sessionhosts-subnet(10.0.1.0/24)** *(choose from dropdown)*
   - Specify Domain or Unit: **No**
 
   ![ws name.](media/ch2.png)
 
  **C**. Administrator Account details:
  
   - AD domain join UPN: *Paste your username* **<inject key="AzureAdUserEmail" />**
   - Password: *Paste the password* **<inject key="AzureAdUserPassword" />**
   - Confirm Password: *Paste the password* **<inject key="AzureAdUserPassword" />** *again.*
   
   ![ws name.](media/w2.png)
   
> **Note:** This Administrator Account details will be used for domain joining the virtual machines to the Windows AD domain that we created using AADDS.
   
7. Click on **Next: Workspace** to proceed. 

8. In the Workspace section, we need to specify if we need to register the default application group to a workspace. 

   - Register desktop app group: *Choose* **Yes** 
   - To this workspace: *Click on* **Create new**

   ![ws name.](media/67.png)
   
9. Once you click on **Create new**, a small window pops up where you can specify the Workspace name you are going to create.  

   - Workspace name: **WVD-WS-01** 
   - Click on **OK**
     
   ![ws name.](media/68.png) 

10. Next, click on **Review + create** on the bottom left corner. 

    ![ws name.](media/69.png)


11. The last window helps us to verify if the parameters we filled are correct. Wait for the validation to pass, and click on **Create** to initiate the deployment. 

    ![ws name.](media/ch4.png)

> **Note:** The deployment will take about 30 minutes to succeed.

12. Once it is done, open notifications by clicking on the **bell icon** and click on **Go to Resource**.  

    ![ws name.](media/71.png)

> **[Optional]**
>
> **Note:** In case the previous deployment for Host Pool fails, follow the below steps. Else, continue from step 13:
>
>i.   Go to the **WVD-RG** resource group and click on **Overview**.
>
>   ![ws name.](media/w15.png)
> 
>ii.  Select the **resources highlighted (1)** in the image below. Next, click on the **ellipsis (2)** in the top-right corner and click on **Delete (3)**. Make sure you **DO NOT** delete any other resources other than the ones highlighted in screenshot below.
>
>   ![ws name.](media/w27.png)
>
>iii. Once you are on the Delete Resources screen, type **yes** under _Confirm delete_ text bar and click on **Delete**
> 
>   ![ws name.](media/w28.png)
>
>iv.  Once the resources are deleted perform steps 1 to 11 under **Task 2: Create Host Pool**.
>
>v.   Now wait for the deployment to succeed. Once done, open the notifications and click on **Go to Resource**.  
>
>   ![ws name.](media/71.png) 

13. You will see that the host pool **WVD-HP-01** is created with two session hosts in it and a default application group (of type Desktop).  

    ![ws name.](media/w29.png)

14. Now click on **Session Hosts** from under the **Manage** blade. Here you can view newly created session hosts. 

    ![ws name.](media/86.png)

15. Click on the **Next** button present in the bottom-right corner of this lab guide.  

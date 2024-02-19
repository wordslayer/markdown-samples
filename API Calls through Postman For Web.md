# API Calls through Postman For Web
### **Overview**

Postman is a free program that allows you to manage, save, and make API calls for a more streamlined experience. In this tutorial, we will cover how to set up your first API call in Postman using the Constellix DNS API Collection.

----------

## **Common Use Case for Using Postman**

[Postman](https://www.postman.com/product/what-is-postman/)  is especially helpful for API testing and management and is much less tedious than running curls by hand in a terminal. With this tool, you can analyze APIs created by someone else or test your own.

----------

### **Prerequisites**

-   You already have a  [Postman](https://identity.getpostman.com/login)  account
-   You have created a Workspace in Postman or are using the default workspace (Personal or Team)
-   You have already  [generated API keys](https://support.constellix.com/support/solutions/articles/47001200127-how-to-generate-an-api-key)  in Constellix

----------

## **How to Make Constellix API Calls Through Postman For Web**

**1. Sign In to Postman**

Open Postman and log in to your account.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115546001/original/XoN-q_CXDRdgj8Pi1-YKG9yOxFp9sCWQKw.png?1640697774)

### **2. Open Constellix API Page and Run Postman**

In a new tab or window, open the  [Constellix API Documentation](https://api-docs.constellix.com/?version=latest)  page. Click the orange  **Run in Postman**  button at the top-right of the screen.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115546120/original/CvY7FIvWzF-c_yFy3sdEDOaviHrfWPNt6w.png?1640697829)

### **3. Choose How You Want to Run Postman**

In the  **Run in…**  window, choose where you want Postman to run:

Postman for Web (Supported only for Chrome, Firefox, Edge)

Postman for Windows (Mac or Linux, depending on your machine)

In this tutorial, we will be using  **Postman for Web**  on  **Chrome**.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115546321/original/Dum8_Bx4w8GzMOml-2MT_ZmQq7thlWaTog.png?1640697888)  

Once you make your selection, you will be directed to the following page:

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115546492/original/4G8M3LsC9v7ptXByZ5uF9PREufweD4ZejQ.png?1640697962)

### **5. Retrieve Constellix API credentials**

In a new tab or window,  **retrieve your API credentials**  by accessing the Constellix User Management Console.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115548189/original/1nXSsDxLzztSnZPVGbk1mXV9guEnX-fWOA.png?1640698539)

----------

> If you have not yet generated an API key, visit our  [How to Generate an API Key](https://support.constellix.com/support/solutions/articles/47001200127-how-to-generate-an-api-key)  tutorial.

----------

### **6. Import Collection**

Before you can create a new environment, you will need to  **Import the Contellix API**  collection to a workspace. Choose a workspace and then click the orange  **Import** button.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115548661/original/pppMVLCr391yXzexbioTDQj7L-SuCkUHdg.png?1640698697)  

### **7. Enter Workspace**

From the top left menu, click on  **Workspaces**, and then select the workspace you wish to use.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115548843/original/ZGKV6pqZYFbxSY3CZOnoUtTwoiaA1URReQ.png?1640698736)

### **8. Create New Environment**

Once in your workspace, you should see that the Constellix DNS API Collection was added to your Activity list.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115549112/original/0izMJP_OgJlY3WaL8Pk2Lg59x6lGAgjp6Q.png?1640698818)

To create a new environment, press the  **Environment** button located in the left-hand menu and then click the  **+ icon**.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115549227/original/sydKj1Oh9ztPbs2xQ8oh5JrJfgBeryng5g.png?1640698850)  

>**Optional** (but recommended): Rename your environment by clicking the horizontal  **ellipsis** to expand options, and then choose  **Rename** (for this tutorial, we renamed the environment Constellix API).

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115549396/original/Q9D-K5wnHqqlMStnIEycRZWIYHOVJQKBLg.png?1640698900)  

### **9. Add New Variable and Enter Constellix API Key in Postman**

First, enter the word  **apiKey** (case sensitive) into the  **Variable field in Postman**. Next, enter the  **actual API Key**  into the **Initial Value**  field. Once entered, the  **Current Value**  field will be auto-populate with the key information.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115549722/original/ye2GBqM5JLAGU39K9K24fmze4n2qDlXzyQ.png?1640698953)

### **8. Add New Variable and Enter Secret Key in Postman**

Enter the word  **secretKey**  (case sensitive) into the Variable field in Postman. Next, enter the  **actual Secret Key**  into the  **Initial Value**  field. Once entered, the  **Current Value**  field will auto-populate with the secret key as well.

Next, click  **Save** on the right-hand side of the screen to save the keys in Postman.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115549935/original/o6iw6Fioj-mcKB515qtyazzPRd26bP0YEQ.png?1640699031)  

### **10. Navigate to Collections and Choose API Call**

From the left-hand menu, choose the option for  **Collections** (first option), then use the arrow icons to expand the Constellix DNS API options. For this tutorial, we will be using  **Get all Domains**  as an example.

Constellix DNS API > API Calls > DNS > v1 - Version 1 > Domains > Get all Domains.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115551052/original/vmrp70UezStrHrsU3nI2qno5wsBCc-4fYQ.png?1640699408)  

### **11. Click Get All Domains API Call Option and Send**

Once you have found the API call you want to use, click on Get All Domains (or whichever call you chose).

After clicking Get All Domains, the necessary URL for the API call  **auto-populates**. Click the blue  **Send** button to complete the API call.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115551176/original/cVXWq1vYRVgp_-gMnJqVlvSzK0eA9jvoBA.png?1640699454)

----------

>**Tip**: If you get an error after clicking Send, be sure you actually saved your keys in Postman (see step 8).

----------

You should now see all your domains, domain IDs, and much more information in JSON format.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47115551514/original/wZmc7m-Ya0XNpo2N34mJHZdLO5jKjX5aXw.png?1640699505)  

Visit our website for more information on our  [services and features](https://constellix.com/products/more-features).

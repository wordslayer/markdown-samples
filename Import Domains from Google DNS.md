
# Import Domains from Google DNS

### **Overview**

Constellix offers API integration with major providers such as Google DNS, AWS, and Azure. In this tutorial, we will walk you through the process of importing a domain from Google DNS into Constellix’s Traffic Management system.

----------

> Several steps in this tutorial will take place in Google DNS. We will touch on these steps, but for detailed information, refer to  Google’s documentation. Keep in mind that if Google changes anything in its interface, it may not be immediately reflected here.

----------

**Common Use Cases for Importing Domains from Google DNS**

Importing a domain using API credentials allows you to transfer your domain information quickly and efficiently. This is useful for when you are switching providers or want to set up a secondary DNS configuration with Constellix.

----------

> Constellix does not support traditional Secondary DNS. Instead, secondary configurations are Primary/Primary and are achieved through API. This setup will provide your domain with two authoritative nameservers that are always active.

----------

### **Prerequisites**

-   You have a domain in Google that you want to import into Constellix
-   You have a basic understanding of API calls
-   You are familiar with Google’s Cloud DNS interface

----------

## **Preparing to Import Domain On Google Cloud DNS**

### **1. Log in to your Google Cloud account.**

To begin, log in to your Google Cloud account and navigate to the  **IAM Permissions**  page. This will allow you to create roles and permissions.

Select the  **IAM Permissions**  option from the left-hand menu under “all products” from the main Google dashboard.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090171331/original/j8_gqChLJztKO4S7i5sk3unKQl8rjbdUYg.png?1629201812)  

### **2. Add member**

To add a member, click on the  **ADD person**  button from the IAM & Admin menu at the top of the screen.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090171970/original/1-aapoiDkIgBzAvYrWlLI38zw679k6SEfg.png?1629201965)  

### **3. Assign Member/Role to Your Google Project**

Before importing your domain into Constellix, you will need to add a member/role to your Google Project. To do so, click on  **Manage Resources** near the bottom of the left-hand menu of the IAM & Admin area.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090172780/original/AQYNUkG9wPwbCvgzVdj_62yT5V2TLlK3aQ.png?1629202197)  

### **4. Select Project**

Check the box next to the appropriate project name and then click the white  **Add Member**  button on the far right of the screen.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090174531/original/qtS_0gSvX80ZurLBOBCi-0VOdygHrlHqaw.png?1629202652)  

### **5. Assign role and Permissions**

In the  **Edit permissions**  window, click on the  **Role dropdown**  option to expand choices and choose the appropriate role for the member. You can type the role in the Filter bar to narrow down options, select from the Quick Access options, or scroll through all roles. For example purposes, we selected the Editor role.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090177419/original/rKw537aKaMTBvN-ObvOsjdBiK1BK_9klsQ.png?1629203301)

----------

> For more detailed information about Roles and Permissions, please refer to  [Google’s documentation](https://cloud.google.com/iam/docs/creating-custom-roles?_ga=2.152496381.-536856063.1628856919&_gac=1.157871816.1628856949.CjwKCAjwsNiIBhBdEiwAJK4khkNOPNkqFxNBJGUAqFsEPwW_WLDDt_zqwAQC-_d6qvvPpcWJyJoCVhoCeeQQAvD_BwE).

----------

To save your new member and role, click the blue  **Save** button on the left side of the Add members window.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090179025/original/D0BtjqrTmMSsZWQfGu1ESSlB5O1NZi7JIQ.png?1629203597)

**6. Add Conditions (optional)**

After choosing your role, you can add a Condition. Click  **Add condition**  to see available options. Please see  [Google Cloud’s documentation](https://cloud.google.com/iam/docs/conditions-overview?hl=en)  if you need help with creating conditions.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090180125/original/ox_XWZvnG3SfDncZFqWJpWAe2MiVAKhKqA.png?1629203758)  

Once added, you will see the members and their roles listed when managing your resources for a project.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090180485/original/vllHauJVVKzYDzt0mWGhwR23n_nwfEgYUQ.png?1629203841)

----------

  

> If you need help with Google API options, visit their  [API documentation](https://cloud.google.com/apis/docs/overview?visit_id=637644649459957549-4166835483&rd=1).

----------

### **7. APIs Overview in Google**

From the main Google dashboard, click on Go to **APIs overview**  to access the API page (API page can also be accessed from the menu on the left).

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090182646/original/1xoAiTRKz6lF4gv2wosuqxnJ1OvEy_HocQ.png?1629204354)  
**8. Navigate to the Credentials Dashboard in Google**

From the API page, select the option for  **Credentials** in the left-hand menu.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090182890/original/syLhRf0liN0jSNM-FuKIHo4fvU3d6XwulQ.png?1629204433)

### **9. Create Credentials**

Once in the Credentials area, select  **+ Create Credentials**  in the top menu.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090183088/original/WbI0I5YTPxvpOYYreMHKmTeIhvEoBWyAMg.png?1629204471)  

### **10. Create Service account**

From the dropdown menu, select the option for  **Service account**.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090184654/original/SyfZptDmifpjkUH9tpgRFUQMkAXLUPfxjQ.png?1629204777)

Once you have created a Service account in Google, check the box next to the  **account name**  and choose  **Manage Keys**  under the menu in the Action column.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090184857/original/K1VuV5Q-yqjve0UwaXpzoxdLPYr9rm1GFQ.png?1629204810)

**11. Create Key**

In the Key area, click on the white  **Add Key**  button and select  **Create new key**.

----------

>If you have already created a JSON key, skip to **step 13.**  

----------

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090185654/original/QGZGBBG6KyKt1rJWgZ_q8CJakbqzzXzQCA.png?1629204963)

**12. JSON Key**

Ensure the option for  **JSON** is selected, and then click  **Make Key**. This will prompt you to save the JSON file on your computer. Choose where you want to save the file on your computer, then click  **SAVE**.

You will see a message confirming the file has been saved to your computer. Click  **Close**  to dismiss the message.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090185888/original/_ofKwEEsrhFggkzApfBNqkCpzVeDAYZ4fw.png?1629205022)

Your key should now be showing as  **Active** under Status in the Key dashboard.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090186032/original/9pQIuv_2axoZcevj57Eqz7r_nKF9TZv1WA.png?1629205053)

----------

> **Important**: Make sure your API has been enabled in your Google Cloud account before moving on to the next step.

----------

### **13. Copy JSON Value**

Next, open the JSON file you saved to your computer with any text editor (notepad on PC or Text Editor on Mac, etc.) and  **copy the JSON value**.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090187786/original/4FB-A6-c8iK8qQ6V4q8iuV18JrBQDS0fug.png?1629205471)
  
## **Preparing to Import Domain in Constellix**

**14: Log into Constellix DNS**

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090186393/original/p-pLXO6K8nq69oN1eWYnsnHYwv58Jk9qQg.png?1629205130)  

**15. Select 3rd Party Import**

Once inside the Constellix DNS dashboard, click on  **Configuration** in the left-hand menu and then choose  **3rd Party Import**.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090186558/original/w9TEDe5VbvTI_HIi7zkkRIICJugGwhI5FQ.png?1629205168)  

### **16. 3rd Party Import in Constellix**

Next, click on the gray  **+ icon**  to expand Google DNS API options.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090186683/original/-dQtHIYfHMZaVlocoCx8CfC7qARaq7X0xQ.png?1629205213)  

### **17. Enter Values into Constellix**

Enter the Google  **project ID**  and the  **JSON** values and then click the green  **Continue** button.

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090186942/original/HnlsmuuUjhXA30qhUz4FpPDau7kocazh-A.png?1629205269)  

### **18. Import Domain**

You will now be taken to the  **Import Domain page**  in Constellix. You will see all domains available for importing, as well as a list of those that cannot be imported.

----------

> We do not have a domain managed by Google Cloud, so the screenshot below is just for example purposes of what page you should be on once you have entered your JSON values.

----------

![](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47090188504/original/mBRKFqI3wphwzIG4m3UGwoOXGwlgXjtImw.png?1629205632)  

Once you have selected the domain you want to import into Constellix, click the green  **Continue** button to complete the import.

Visit our website for more information on our  [services and features](https://constellix.com/products/more-features).

# Add A Domain Using Advanced Settings

### **Overview**
This guide shows you how to add a domain to your DNS Made Easy account using advanced settings and features.
>You can add up to 1,000 domains at once. Advanced settings will be applied to each domain being added and will be identical for every domain. For any domain that requires further customization, you can alter the settings individually once the domains have been imported into the DNS Made Easy system.

### **Prerequisites**
- You have a hosted domain ready to add to your account
-   An  [](https://cp.dnsmadeeasy.com/dns/transferAcl) [](https://cp.dnsmadeeasy.com/dns/transferAcl)[ACL has been configured](https://support.dnsmadeeasy.com/support/solutions/articles/47001191946-set-an-access-control-list-for-a-user)[](https://cp.dnsmadeeasy.com/dns/transferAcl) [](https://cp.dnsmadeeasy.com/dns/transferAcl)  in your account (optional)
-   You have already set up  [folders for users/groups](https://support.dnsmadeeasy.com/support/solutions/articles/47001001028-sub-users-groups-and-permissions)  in your account (optional)
- -   You already have a  [](https://cp.dnsmadeeasy.com/dns/soa) [](https://cp.dnsmadeeasy.com/dns/soa)[custom SOA Record](https://support.dnsmadeeasy.com/support/solutions/articles/47001001671-soa-start-of-authority-record)[](https://cp.dnsmadeeasy.com/dns/soa) [](https://cp.dnsmadeeasy.com/dns/soa)  in your DNS Made Easy account (optional)
-   A  [template](https://support.dnsmadeeasy.com/support/solutions/articles/47001001642-create-a-template) has already been created in your DNS Made Easy account (optional)

### How to Add a Domain to Your DNS Made Easy Account
1. **Navigate to Managed DNS**
After logging into your account, select `Managed DNS` from the DNS dropdown menu.

![enter image description here](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47113285733/original/E8dR6AqY6yFgFaxTl8e-Ksm3UHsWUGxMkA.png?1639512023)

2. **Add Domains**
Once in the Managed DNS portal, click on the **Add Domains** button on the right-hand side of the screen.

![enter image description here](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47113285812/original/QNqwdeQbT39ScL7wT_B6LgNHi83N-62yCg.png?1639512049)

**3. Enter your Domain Name(s)**

In the  **Add Domains**  window, type or copy/paste the domain(s) you are adding into the  **Domain Names field**. Domains can be entered in list format or separated by commas, as shown in the examples below.

> Internationalized domain names (IDNs) should be entered using  ==[Punycode](http://www.charset.org/punycode.php).== For example, if your domain name was mañana.com, you would add the domain in DNS Made Easy as “xn--maana-pta.com” (without the quotes). 

![enter image description here](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47113286578/original/KIaRLBX2iWGdLkfOAtailWHc1KDT8PBlrQ.png?1639512317)

**4. Apply Advanced Settings**

After you have entered all the domain names you want to add to your DNS Made Easy account, you can apply  **advanced settings**.

![enter image description here](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47128077456/original/bAPL5Aa3QxdYYsUJl-JM1wSq6pR1UzsK8Q.png?1646055651)

**A. Global Traffic Director:**

Check the box next to  [Global Traffic Director](https://dnsmadeeasy.com/services/globaltrafficdirector/)  if you’d like different query responses based on region.

**B. Applied Template for DNS Records:**

Using templates lets you apply the same standards and configurations to all of your domains at once. If any changes are made to your template, then it will update all records that use the template.

If you have previously  [created a template](https://support.dnsmadeeasy.com/support/solutions/articles/47001001642-create-a-template)  in your DNS Made Easy account, the template will also be shown in this list. In the example below, “test” is a template created based on a domain already in a DNS Made Easy account.

![enter image description here](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47113286865/original/4CRBDmKyGEOV98XZmq_n7JvWT9h88-HgFQ.png?1639512431)

**C. Vanity Name Server Configuration:**

The Vanity NS Config option allows you to rebrand or white label our nameservers for brand recognition. This feature is also ideal for web hosting companies or for security purposes if your servers are on-site.

**D. Custom Start of Authority (SOA) Record:**

At DNS Made Easy, we provide you with a preconfigured SOA record that follows DNS best practices, or you can customize your SOA record to your exact specifications.

![enter image description here](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47113286924/original/RNB8XHpCigeunxhQx804hKBFGwxtW_LlVQ.png?1639512449)

**E. Zone Transfer (AXFR ACL):**

The AXFR ACL option lets you duplicate DNS records without editing information on multiple servers. Any changes made through our control panel or API will automatically send out a notification, which will trigger an IXFR/AXFR transfer between all nameservers so that the same records will be propagated everywhere. To apply this option, you must first configure an Access Control list in DNS Made Easy.

**F. DNS Permissions Folders:**

The folder feature allows you to group users within your organization into permission-based segments. You can configure unique read/write privileges for each domain. Here is a tutorial on how to set up user permissions in your DNS Made Easy account.

**G. DNS Record Import:**

This option allows you to copy DNS records from an existing template or domain in DNS Made Easy. If supported by your previous provider, you can also transfer your records from an external domain via IXFR/AXFR.

![enter image description here](https://s3.amazonaws.com/cdn.freshdesk.com/data/helpdesk/attachments/production/47113287001/original/A5PvktPt2GstZyTeB-gGseIgTc11-JosjA.png?1639512478)

### **5. Complete Add Domains**

Once you have applied your desired settings, click the  **OK** button at the bottom of the window to add the domain(s) into DNS Made Easy.

Visit our website for more information on our  [features and services](https://dnsmadeeasy.com/services/).

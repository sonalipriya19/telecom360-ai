What is multi-tenancy?
ANS: Multi tenancy is the type of arcitecture where multiple tenants(customers) share and use the single instance of infrastructure and software. The users share the same servers, CPU and other infra but their own configuration, data and code remains in their own private org.
---------------------------------------------------------------------------------------------------

Why do Governor Limits exist?
ANS: Salesforce follows a multitenant shared architecture i.e multiple customers share the same CPU, Database and other infrastructure. Hence Salesforce introduced the concept of Governer Limit to control the usage of shared resurces by each indivisual org so as to not adversly affect the performance and stability of all the other tenants. Governer limit ensure that all the orgs get a fair alloction of memory and computing resources.
--------------------------------------------------------------------------------------------------

What is metadata and why it is Salesforce's biggest Strenght?
ANS:  In generic terms, metadata means data about data like in Salesforce when a developer creates say a custom object, Salesforce does not expects the dev to hardcode the custom objects name in the apex code or if we come to think how does Salesforce know about our org's custom data. For this Salesforce uses the concept of metadata, it store the definition of our custom obejcts like its fields, layout, flows, validation rules etc. 

The metadata driven achitecture helps Salesforce to separate our configuration completly fro the platform code and that helps Salesforce to deliver quicker upgrades accross all tenants without affecting each indivisual's configuration. It also helps Salesforce Admins and Devs to build complex database structure, custom pages using drag and drop logic with tools like Salesforc flows which in turn speeds the GTM for any salesforce based application.

It also helps Salesforce to enforce a highly secure multi tenancy on the platform and the system dynamically renders a unique user interface and data view based solely on the matadata of the logged in user.

Usage of metadata also helps the business to kee their entire business setup in atext like metadata file which can be easily copied and deployed to lower sandboxes for testing as well and ensure a smooth production deployment.
-------------------------------------------------------------------------------------------------

If metadata is so powerful, why does not Salesforce store business data (like accounts and conytacts) as metadata too? Why are metadata and business data treated differently?

Salesforce separates metadata from business data because they have different characteristics and usage patterns. Metadata defines the application's structure and behaviour - such as objects, fields, page layoutm flows and security configuration and changes relatively infrequently. This allows Salesforce to cache metadata aggressively, improving platform performance and enabling safe platform upgrades. Business data on the other hand consists of customer
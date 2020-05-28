
# Salesforce Marketing Cloud Setup Guide

Follow our setup guide to connect **Salesforce Marketing Cloud**  to **SkyPoint**.

You need to provide the following details:

  1. **Client Id**
  1. **Client Secret**
  1. **Authentication URL**
  
  Once you enter all the required details, **Click Connect**: 
  
   * Upon clicking the Connect button, it will validate your credentials, if it is successful you will see a notification **Data loaded successfully** else it will show the error that login has failed.

   * Upon successful connection, it will show the names of all **Subscriber Lists** and **Campaigns** imported from the source with headers like Name, Type, Entity Name etc.

   * Select the **Subscriber Lists** and **Campaigns** you want and save the data flow.

   * You can **Run** the data flow as and when required by choosing the **Run action** from dataflow screen.

### Obtain Client ID and Client Secret from Salesforce Marketing Cloud

Perform the following steps to retrieve the **Client ID** and **Client Secret** for a new package:

1.  Log in to **Salesforce Marketing Cloud**.

2.  Go to **Setup >> Apps >> Installed Packages**

3.  Click **New** to create a new package.

4.  In the New Package Details window, enter the name and description for the package.

    To use OAuth 2.0, select **Create with enhanced functionality (recommended)**.

5.  Click **Add Component**.

6.  Select **API Integration** as the component type.

7.  Click **Next**.

8.  Select **Server-to-Server** as the integration type.

9.  Click **Next**.

10.  Select the following **Permissions for the Server-to-Server properties:**

> For both import and export integrations workflows of SkyPoint and Salesforce Marketing Cloud, client keys will need the following access permissions:    

|Workflows  |Permissions  |
|---------|---------|
|Contacts - List and Subscribers   | Read, Write |
|Hub - Campaigns  | Read, Write |
|Data - Data Extensions   | Read, Write |
|Data - Tracking Events   | Read, Write |
|Provisioning - Accounts   | Read, Write |
|Automation - Journeys   | Read, Write |
|Contacts - Audiences   | Read, Write |
|Channels - Email  | Read, Write |
|Marketing Cloud Connect  | Read, Write |
    
11.  Click **Save**.

    The Components section displays the Client ID and Client Secret for the package.    

Perform the following steps to retrieve the Client ID and Client Secret for an existing package:

1.  Go to **Setup >> Apps >> Installed Packages**

   

    The Installed Packages page lists all the packages installed in the Salesforce Marketing Cloud account.

    

2.  Select a package and go to the **Components** section.

    

    -   To add a new component, click **Add Component**.

    -   To edit existing component, click **Edit**.

    The Components section displays the Client ID and Client Secret for the package.

3.  Click **Save**.

If an existing package uses OAuth 1.0, you cannot edit the package to use OAuth 2.0. You must create a new package to use OAuth 2.0. SkyPoint recommends that you upgrade to OAuth 2.0 before Salesforce Marketing Cloud drops support for OAuth 1.0.

For information about configuring installed packages and API integration, see the following URL: [https://developer.salesforce.com/docs/atlas.en-us.noversion.mc-app-development.meta/mc-app-development/index.htm](https://developer.salesforce.com/docs/atlas.en-us.noversion.mc-app-development.meta/mc-app-development/index.htm)
Select API Integration as the component type.

### Dealing with **Data Extensions**

A data extension in Marketing Cloud Email Studio is a table within the application database that contains your data.
It has constraints like that, name of the data extension and column names of the data extensions can not start with underscore ( _ ) else it will throw error. 


Refer below links for data extension creation and its constraints.


[Data Extension Creation](https://help.salesforce.com/articleView?id=mc_es_create_data_extension_classic.htm&type=5)


[Data Extension Name Constarints](https://help.salesforce.com/articleView?id=mc_es_data_extension_error_messages.htm&type=5)


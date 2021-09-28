# Yuyutsu
SAP Cloud Integration Tool

A very beautiful app to transport Cloud Integration artifacts from one tenant to another. Not just transport, you can generate comparison report and view the exact difference between source and target artifacts till code level. So to make sure, what exactly you are transporting.

> Available for both Mac and Windows 
> As this is my personal project and executables are not signed, you will get warning before installing it. I have made sure that the app only makes the connection to SAP Cloud Integration tenants. And most important, passwords are saved in OS specific vaults, i.e. for Windows it uses Credential Vault and for Mac OS it uses Keychain.

![alt text](https://github.com/lalit2054/yuyutsu/raw/main/screenshots/main.png)

## Highlights
- **Tabbed based explorer**<br>
- **Search packages across environments**<br>
- **Compare artifact versions between two environments**<br>
- **Compare code**<br>
- **Compare configurations**<br>
- **Update configurations**<br>
- **Transport artifacts**<br>
- **Single click express Transport, Update Configs and Deployment**<br>

## Manage Connection

This tab is used to manage connections to different tenants. In order to secure the passwords, they are saved in Keychain for Mac OS and Credential Vault for Windows, password store for respective OS.

- Click Add connection 
  - Enter Connection Name - Name should include only letters, numbers and underscore
  - Host - Enter CPI Host address
  - User Name
  - Password
  - Confirm Password
  - Type - Type of environment, options are Dev/Test/Quality/Production
  - Save - App will verify the connection when you click this button and it will be saved
- Add atleast two connections for Transport to work<br>
- Select one connection and add Targets from section at the right side<br>

![alt text](https://github.com/lalit2054/yuyutsu/raw/main/screenshots/connections.png)

## View Packages

This tab is used to view the packages for the selected connection. This is the place where you can select one of packages to transport its artifacts.

- Select a connection to view the packages<br>
- Expand the package to view artifacts belongs to that package<br>
- Click transport icon to jump to Transport Tab for that package<br>

![alt text](https://github.com/lalit2054/yuyutsu/raw/main/screenshots/packages.png)

## Transport Package

This tab is most important one to perform different types of action. 

- Select source and target connections to view comparison report of all the artificats of the package<br>
- There are three views available for the comparison report<br>
  - Diff view (Default) - This view will show the artifacts where source version and target version are different. This helps user to quickly identify the relevant artifacts which are mostly to be transported.
  - Full view - This view will show version comparison for all the artifacts.
  - Draft view - This view will show all the artifacts which are still in Draft state
- The artifacts which can be transported will have four action buttons
  - Compare code - Here you can compare the code of each file of the artifact. 
  - Configurations - Here you can compare the configurations available on source and target tenants.
  - Transport - This will transport the artifact to the target tenant.
  - Transport and Deploy - This will transport as well as deploy the artifact in the target tenant.

![alt text](https://github.com/lalit2054/yuyutsu/raw/main/screenshots/packageTransport.png)

## Code comparison

Here you can compare the code of the artifact. The contents of the Target environment is shown on left side while for Source environment, its shown on right side. This works exactly like Git, where lower verion is shown on left and higher on right, so you can view the changes done on top of lower version.

- You have two views to choose from
  - Side by Side (Default) - Two sections to show code differences
  - Inline View - Inline code differences are shown
- Folder view of artifact is shown on the left side 
  - File with different content on source and target tenants are marked as **distinct**
  - New files added will be marked as **added**
  - Missing files will be marked as **missing**

![alt text](https://github.com/lalit2054/yuyutsu/raw/main/screenshots/codeview.png)

## Configuration comparison

Here you can compare the configurations present in source and target tenants. 

- You have two views to choose from
  - Diff view (Default) - This view shows configurations whose values are different in both the tenants
  - Full View - This view view will show all the configurations.
- Update the configuration values that you want to set in the input field for target tenant.
- You can use **Transport** or **Transport and Deploy**. This will also update the configurations.
 

![alt text](https://github.com/lalit2054/yuyutsu/raw/main/screenshots/configview.png)

## Search Panel

The very initial version of global search, as of now supports searching only Packages across different tenants. In future more powerful search functionality will be delivered with this panel. Click any of the packages and you will be redirected to Transport package tab.

![alt text](https://github.com/lalit2054/yuyutsu/raw/main/screenshots/search.png)

## Notification Tab

A very informative tab to show all the peristent notifications. A very beautiful timeline of the activities happened during the task will be shown. The notification will be automatically removed after 4 days.

![alt text](https://github.com/lalit2054/yuyutsu/raw/main/screenshots/notification.png)

## App updates and Bug Report

Click Bug and you can perform following actions -

- Check for updates - 
  - Windows OS - It will allow to download and apply the updates.
  - Mac OS - It will redirect to downdload page if updates are available.
- Report Bug
- Request Feature
- Provide Feedback

![alt text](https://github.com/lalit2054/yuyutsu/raw/main/screenshots/bug.png)


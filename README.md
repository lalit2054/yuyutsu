# Yuyutsu
SAP Cloud Integration Tool

> Available for both Mac and Windows 

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

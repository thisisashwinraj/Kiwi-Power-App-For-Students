# Kiwi - Power Application for College Students
Kiwi is a power application integrated with power automate, sharepoint and other azure services, for students to access all information pertaining to their academics at one place.The application will serve as a one stop destination for all student services, above and beyond. The project is licensed under the Creative Commons Zero v1.0 Universal License. The application hosts a wide array of features including attendance records, bus routes and college schedule amongst others. The latest released stable version of Kiwi is 1.0.1

The project started in December 2021 as part of Microsoft's future ready talent program. All app resources and pull requests are maintained and reviewed by volunteers. Learn more about Kiwi v1.0.4 here.

# Subdirectories and Constraints

### App Dependencies:
- **Application:** Power Apps, Power Automate, Power BI
- **Data:** Office365Users, Office365Outlook, SharePoint

**Note:** Kiwi runs on all operating systems, is quick to install and is available for free use. Various features of the application have been extended using Azure. To use the application, the user shall have access to the Microsoft 365 admin centre with global administrator or billing administrator roles or shall possess an Azure subscription.

### Files and Folders:
The files and folders present in this power application are as described:
- **Assets:** This directory contains the graphic images used in the application. Imgbot is used to optimize these graphics.
- **Connections:** This directory includes the files of all the connection instances that are used by the power application.
- **DataSource:** This directory includes all the storage group files that are integrated and used by the power application.
- **Entropy:** Volatile elements (like timestamps) are extracted to this file. This helps reduce noisy diffs in other files.
- **Packages:** It contains a downloaded copy of external references, templates, API Definition files, & component libaries.
- **Src:** It includes the control and component files of the application - each app screen has a seprate **.fx.yaml** file.
- **StableVersions:** This directory includes all of the stable releases of the kiwi application, including its source code.
- **CanvasManifest.json:** The app manifest file includes the header propertis and the publish information of the power app.

# Kiwi - Power Application for College Students
Kiwi is an application integrated with power automate, sharepoint and other azure services, for students to access all information pertaining to their academics at one place. This application will serve as a one stop destination for all the student services, above and beyond. The project is licensed under the Creative Commons Zero v1.0 Universal License.

The project started in December 2021 as part of Microsoft's Future Ready Talent program. All app resources and pull requests are maintained and reviewed by a team of volunteers. Learn more about the features of Kiwi app v1.0.1 here.

# Subdirectories and Constraints

### App Dependencies:
- **Application:** PowerApps, Power Automate, Power BI
- **Data:** Office365Users, Office365Outlook, SharePoint

**Note:** Kiwi runs on all the operating systems & environments. The app is quick to install & available for free use. The various features of the application have been extended using Azure. To use the application, the user shall have access to the Microsoft 365 Admin Centre with global or a billing administrator roles or shall possess an Azure subscription.

### Files and Folders
The files and folders present in the power application repository are as described:
- **Assets:** This contains all graphic images used in the application. Imgbot is used to optimize these graphics.
- **Connections:** This includes the files of all the connection instances that are used by the power application.
- **DataSource:** This  includes all the storage group files that are integrated and used by the power application.
- **Entropy:** Volatile elements (like timestamps) are extracted to these files. This reduce noisy diffs in other files.
- **Packages:** It contains downloaded copy of external references, API Definition files, and component libaries.
- **Src:** It includes the control & component files of the application, each app screen has a seprate **.fx.yaml** file.

# User Installation and Source Code
The application is supported across all mobile devices - iOS(iOS 14 or later) and Android(Android 9 or later). The app can also be run over web and windows(Windows 8.1 or later, depending on your plan). For privileges required to run model-driven apps on Power Apps Mobile app, see [required privileges](https://docs.microsoft.com/en-us/dynamics365/mobile-app/set-up-dynamics-365-for-phones-and-dynamics-365-for-tablets#required-privileges).

To run the application, first download PowerApps for mobile device. For iOS (iPad or iPhone), go to the [App Store](https://itunes.apple.com/app/powerapps/id1047318566?mt=8) and for Android, go to [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.msapps). Open Power Apps on your mobile device, and sign in by using your personal Azure Active Directory credentials. After logging in, find and tap on the Kiwi App logo to open the applications and Sign In.

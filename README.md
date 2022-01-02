# Kiwi - Power Application for Students
Kiwi is an application integrated with power automate, sharepoint and other azure services, for students to access all information pertaining to their academics at one place. This application will serve as a one stop destination for all the student services, above and beyond. The project is licensed under the Creative Commons Zero v1.0 Universal License.

This project started in December 2021 as part of Microsoft's Future Ready Talent program. All app resources and pull requests are maintained and reviewed by a team of volunteers. Learn more about the features of Kiwi app v1.0.1 here.

# Subdirectories and Constraints

### App Dependencies:
- **Application:** PowerApps, Power Automate, Power BI
- **Data:** Office365Users, Office365Outlook, SharePoint

**Note:** Kiwi app runs on all operating system and environments. This app is quick to install and is available for free use. The various features of the application have been extended using Azure. To use the application, user shall have access to the Microsoft 365 Admin Centre with a global or a billing administrator roles or shall possess an Azure subscription

### Files and Folders
There are a number of app resources and settings that retain their original 'not-meant-for-humans treatment' and are not intended to be edited outside of the PowerApps Studio.  The full directory's structure and how to deal with merge conflicts in other files is outlined in this GitHub readme. The subdirectories critical to the application are as described
- **Assets:** This file contains graphic images used in the application. Imgbot is used to optimize the image files.
- **Connections:** This includes the files of various connection instances that are used by this power application.
- **DataSource:** This  includes all the storage group files that are integrated and used by this power application.
- **Entropy:** Volatile elements (like timestamps) are extracted to these files. This reduce noisy diffs in other files.
- **PackageFiles:** It contains downloaded copy of external references, API Definition file and component library.
- **Src:** It includes all control & component files of the application & each app screen has a seprate .fx.yaml file.

# User Installation and Source Code
The application is supported across all mobile devices - iOS (iOS 14 & later) and Android (Android 9 & later). This app can also be run over web and windows (Windows 8.1 or later, depending on your plan). For privileges required to run a model-driven apps on Power Apps Mobile app, see [required privileges](https://docs.microsoft.com/en-us/dynamics365/mobile-app/set-up-dynamics-365-for-phones-and-dynamics-365-for-tablets#required-privileges). For iOS users, the Power Apps mobile app is also integrated with Siri shortcuts, which gives you the ability to add a shortcut to the Home screen, launch apps with Siri, and create new workflows. This feature requires iOS version 14 and Power Apps mobile version 3.20092.x or later.

### Directory Strudture
Kiwi's development takes place on GitHub. Please submit any bugs that you may encounter to the issue tracker with a reproducible example, demonstrating the problem in accordance with the issue template present in contributing files.
    
    ├── CanvasManifest
    ├── Assets                        // Contains image graphics and custom css
    │   └── Images
    ├── Connections                   // Listing of all data sources in the app
    ├── Data Sources
    ├── Entropy
    ├── Pkgs                          // Contains external reference components
    │   ├── Wadl                      
    │   └── TableDefinitions          // Listing of integrated sharepoint lists
    ├── README.md                     
    ├── Src                           // Contains base level app info and datas
    │   └── EditorState
    ├── ControlTemplates              // Information on the 3 base classes used
    └── ComponentReferences           // Contains the listing of all components

To run the application, first download PowerApps for mobile device. For iOS (iPad or iPhone), go to the [App Store](https://itunes.apple.com/app/powerapps/id1047318566?mt=8) and for Android, go to [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.msapps). Open Power Apps on your mobile device, then sign in by using your university issued Azure Active Directory credentials. After logging in, find and tap on the Kiwi logo to open the application and sign in.
    
# Contribution
New contributors of all experience levels are welcome to contribute to this project. Some basic information about the project has been included in this README. For major changes, it is recommended that you open an issue first (in line with the issue template) to discuss what you would like to change, before proceeding with making a new pull request.

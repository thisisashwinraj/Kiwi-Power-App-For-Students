![](https://github.com/thisisashwinraj/Kiwi-Power-Application/blob/main/Assets/kiwi_banner_light.png#gh-light-mode-only)
![](https://github.com/thisisashwinraj/Kiwi-Power-Application/blob/main/Assets/kiwi_banner_dark.png#gh-dark-mode-only)

Kiwi is an application integrated with power automate, sharepoint, and other azure services, for students to access all information pertaining to their academics at one place. This application will serve as a one stop destination for all the student services, above and beyond. The project is licensed under the [Creative Commons Zero v1.0 Universal License](https://github.com/thisisashwinraj/Kiwi-Power-Application/blob/main/LICENSE).

This project started in December 2021 as part of the Microsoft's [Future Ready Talent program](https://futurereadytalent.in/). App resources and pull requests are maintained and reviewed by a team of volunteers. Learn more about the features of Kiwi app v1.0.1 [here](https://github.com/thisisashwinraj/Kiwi-Power-Application#user-installation-and-source-code).

# SubDirectories and Constraints

### App Dependencies:
- **Application:** Power Apps, Power Automate, Power BI (These front-end tools are part of Microsoft Power Platform)
- **Data:** Office365Users, Office365Outlook, SharePoint (These tools are used for building the back-end architecture)

**Note:** Kiwi app runs on all operating system and environments. This app is quick to install and is available for free use. The various features of the application have been extended using Azure. To use the application, user shall have access to the [Microsoft 365 Admin Centre](https://www.microsoft.com/en-in/microsoft-365/business/office-365-administration) with a global or a [billing administrator](https://docs.microsoft.com/en-us/azure/cost-management-billing/manage/manage-billing-access) roles or shall possess an [Azure subscription](https://azure.microsoft.com/en-us/free/)

### Files and Folders
There are a number of app resources and settings that retain their original 'not-meant-for-humans treatment' and are not intended to be edited outside of the Power Apps Studio.  The full directory's structure and how to deal with merge conflicts in other files is outlined in this GitHub [README](https://github.com/thisisashwinraj/Kiwi-Power-Application#readme). The subdirectories critical to the application are as described
- **Assets:** This directory contains graphic images used in the application. ImgBot is used to optimize the image files
- **Connections:** This include the directories of various connection instances that are used by this power application
- **DataSource:** This directory includes all storage group files, that are integrated and used by this power application
- **Entropy:** Volatile elements (eg: timestamps) are extracted to these directories. This reduce noisy diff in other files
- **PackageFiles:** It contains the downloaded copies of external references, API Definition file, and component library
- **Src:** It includes all control & component files of the application & each app screen has a seprate .fx.yaml directory

All relevant updates and stable versions are made available in the [~/StableVersion](https://github.com/thisisashwinraj/Kiwi-Power-Application/tree/main/stableVersions) sub-directory. Some subdirectories may be sensitive for the project and may trigger review requests, when pull requests touch these files. GitHub handles with commit rights made available in the [~/Template Files/CODEOWNERS](https://github.com/thisisashwinraj/Kiwi-Power-Application/blob/main/Template%20Files/CODEOWNERS) are responsible for reviewing such changes

# User Installation and Source Code
The application is supported across all mobile devices - iOS (iOS 14 & later) and Android (Android 9 & later). This app can also be run over web, and windows (Windows 8.1 or later, depending on your plan). For privileges required to run a model-driven apps on Power Apps Mobile app, see [required privileges](https://docs.microsoft.com/en-us/dynamics365/mobile-app/set-up-dynamics-365-for-phones-and-dynamics-365-for-tablets#required-privileges). For iOS users, the Power Apps mobile app is also integrated with Siri shortcuts, which gives you the ability to add a shortcut to the Home Screen, launch apps with Siri, and create new workflows. This feature requires iOS version 14, and [Power Apps mobile version 3.20092.x](https://learn.microsoft.com/en-us/power-apps/mobile/run-powerapps-on-mobile) or later.

![](https://github.com/thisisashwinraj/Kiwi-Power-Application/blob/main/Assets/Kiwi_MobileApp.png)

Kiwi's development takes place on GitHub. Please submit any bugs that you may encounter to the issue tracker with a reproducible example, demonstrating the problem in accordance with the [issue template](https://github.com/thisisashwinraj/Kiwi-Power-Application/tree/main/Template%20Files/ISSUE_TEMPLATE) present in contributing files.
    
    ├── CanvasManifest
    ├── Assets                        // Contains image graphics and custom css
    │   └── Images
    ├── Connections                   // Listing of all data sources in the app
    ├── Entropy
    ├── Pkgs                          // Contains external reference components
    │   ├── Wadl                      
    │   └── TableDefinitions          // Listing of integrated sharepoint lists
    ├── README.md                     
    ├── Src                           // Contains base level app info and datas
    │   └── EditorState
    ├── ControlTemplates              // Information on the 3 base classes used
    ├── Data Sources
    └── ComponentReferences           // Contains the listing of all components

To run the application, first download PowerApps for mobile device. For iOS (iPad or iPhone), go to the [AppStore](https://itunes.apple.com/app/powerapps/id1047318566?mt=8), and for Android, go to [Google Play](https://play.google.com/store/apps/details?id=com.microsoft.msapps). Open PowerApps on your mobile device & then signin by using your university issued Azure Active Directory credentials. After logging in, find and tap on the Kiwi logo to open the application, and sign in.
    
# Contribution Guidelines and Usage
New contributors, of all experience levels are welcome to contribute to this project. Some basic information about the project have been included in this README. For major changes, it is recommended that you open an issue first (in line with our [issue template](https://github.com/ashwinraj-in/Kiwi/tree/main/Template%20Files/ISSUE_TEMPLATE)) to discuss what you would like to change before proceeding with making a new pull request.

To start contributing to the project, clone the repository into your local system subdirectory using the below git code:
```
git clone https://github.com/thisisashwinraj/Kiwi-Power-Application.git
```
MS App directory contains the .msapp file of the application. Un-pack the msapp file of the latest stable release using the PowerApps Source File Pack and Un-Pack Utility, which is similar to the [Solution Packager](https://docs.microsoft.com/en-us/power-platform/alm/solution-packager-tool) for [Microsoft Dataverse](https://powerplatform.microsoft.com/en-us/dataverse/). To install the tool to your system, clone the [microsoft/PowerApps-Language-Tooling](https://github.com/microsoft/PowerApps-Language-Tooling) into your local computer system:
```
git clone https://github.com/microsoft/PowerApps-Language-Tooling.git
```
The output files (i.e., ".yaml version") have a version number. During preview, the tool is not backwards compatible, so the version used to repack must match the version used to pack. Keep a copy of the original msapp file for future use.

Alternatively, you can also use the [Microsoft Power Platform CLI](https://docs.microsoft.com/en-us/powerapps/developer/data-platform/powerapps-cli#install-microsoft-power-platform-cli), download this tool from here. To unpack .msapp file:
```
pac canvas unpack --msapp FromApp.msapp --sources ToSourceFolder
```

## Generate the Source Code
To be able to use this Power Apps Language Toolkit, you need to install the [VisualStudio Code](https://code.visualstudio.com/) and [.NET Core 3.1(x64)](https://dotnet.microsoft.com/en-us/download/dotnet/3.1). Navigate to the local directory of the cloned Power Apps Language Tool, and run the build.cmd file, as an admin. The command prompt shall open, show a few lines and then close automatically. After the build is complete, you can find a bin folder in this directory containing a debug directory that hosts the PASopa folder. Copy its path <PASopa_Path>

![](https://github.com/thisisashwinraj/Kiwi-Power-Application/blob/main/Assets/kiwiDemo.gif)

Open the command prompt window as an administrator, and navigate to this PASopa directory, using this command:
```
cd <PASopa_Path>
```
Create a new sub-directory, wherein, the source code of this application will be stored <New_Folder_Path>. Copy this path to this folder, and the .msapp file <MSapp_File_Path>. Run this  command, to get your code in the new directory:
```
pasopa -unpack <MSapp_File_Path> <New_Folder_Path>
```
You can now open this subdirectory, in any code editor of your choice (eg. [Sublime](https://www.sublimetext.com/)) and make the necessary changes.

## Submitting a Pull Request
Before opening a Pull Request it is recommended to have a look at the full contributing page to make sure your code complies with all the pull request guidelines. Please ensure that you satisfy the [~/checklist](https://github.com/thisisashwinraj/Kiwi-Power-Application/tree/main/Template%20Files/PULL_REQUEST_TEMPLATE) before submitting your PR.

Navigate to this sub-directory & check status of all files that were altered (red) by running the below code in Git Bash:
```
git status
```
Stage all your files that are to be pushed into your pull request. This can be done in two ways - stage all or some files:
```
git add .            // adds every single file that shows up red when running git status
```
```
git add <filename>   // type in the particular file that you would like to add to the PR
```

Commit all the changes that you've made, and describe in brief the changes that you have made using the command:
```
git commit -m "<commit_message>"
```
Push all of your updated work into this GitHub repo in the form of a Pull Request by running the following command:
```
git push origin main
```
Pull requests are reviewed by the team on a rolling basis. If the team is slow to review your PR either your pull request needs some benchmarking, tinkering &/or convincing. We ask you for your understanding during this review process.

# License and Project Status
The Kiwi App, and all of its resources are distributed under [Creative Commons Zero v1.0 Universal License](https://github.com/thisisashwinraj/Kiwi-Power-Application/blob/main/LICENSE). This app is compatible with all operating systems. The latest released stable version of Kiwi is v1.0.1, and available to be installed on any local system for general use through a website or the app. All new releases are logged in the [~/StableVersions](https://github.com/thisisashwinraj/Kiwi-Power-Application/tree/main/stableVersions)

Upcoming updates will include more features, support for admin logIn, and chat support through [power virtual agent](https://powervirtualagents.microsoft.com/en-us/)

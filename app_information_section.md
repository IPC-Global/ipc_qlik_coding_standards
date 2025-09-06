# App Information Section

## Purpose

The App Information Section begins every Qlik Application Load Script and contains a description of the application and the history of all changes made to the app.

## Instructions

Create a Section called **App Information** before the **Main** Section in any new app. This code records:

- The App name
- A Description of the app
- A version history with change notes

```
AppInformation:  
LOAD * INLINE [  
AppInformation_Name|AppInformation_Description  
Sample Application Name|This app loads data from X, Y and Z tables and creates a data model.  
](delimiter is |);

CodeChange:  
LOAD * INLINE [  
CodeChange_Version|CodeChange_Date|CodeChange_Author|CodeChange_Description  
1.3|10/25/2024|Mark Costa|Added CS-KEYS Section  
1.2|10/22/2024|Mark Costa|Added CS-MAINVARIABLES in the Main Section  
1.1|10/22/2024|Mark Costa|Added CS-COMMENTS Section  
1.0|10/22/2024|Mark Costa|Initial version  
](delimiter is |);

```
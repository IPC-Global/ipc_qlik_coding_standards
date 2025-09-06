# App Information Section

## Purpose

The App Information Section begins every Qlik Application Load Script and contains a description of the application and the history of all changes made to the app.

## Instructions

In the Qlik Applicaiton Load Script, create a Section called **App Information** before the **Main** Section with the following content:

```
AppInformation:  
LOAD * INLINE [  
AppInformation_Name|AppInformation_Description  
<application-name>|<application-description>  
](delimiter is |);

CodeChange:  
LOAD * INLINE [  
CodeChange_Version|CodeChange_Date|CodeChange_Author|CodeChange_Description  
<change-version>|<change-date>|<change-author>|<change-comment>  
](delimiter is |);

```

# Document Conditional Access with PowerShell 

[![PSGallery Version](https://img.shields.io/powershellgallery/v/Invoke-ConditionalAccessDocumentation.svg?style=flat-square&label=PSGallery%20Version)](https://www.powershellgallery.com/packages/Invoke-ConditionalAccessDocumentation) [![PSGallery Downloads](https://img.shields.io/powershellgallery/dt/Invoke-ConditionalAccessDocumentation?style=flat-square&label=PSGallery%20Downloads)](https://www.powershellgallery.com/packages/Invoke-ConditionalAccessDocumentation)

This PowerShell script adapts functionality from the [Modern Workplace Concierge](https://github.com/nicolonsky/ModernWorkplaceConcierge) and documents your Conditional Access Policies. The script exports all the data as a csv file which can be pretty formatted as excel workbook.

1. Install this script from the PowerShell gallery (dependent modules are automatically installed):

    ```Install-Script -Name Invoke-ConditionalAccessDocumentation -Scope CurrentUser```
    
    Script is saved to the user's default script lcoation: ```"C:\Users\%USERNAME%\Documents\WindowsPowerShell\Scripts"```
    
2. Connect to Microsoft Graph

    Grant initial consent: ```Connect-Graph -Scopes @("Application.Read.All", "Group.Read.All", "Policy.Read.All", "RoleManagement.Read.Directory", "User.Read.All")```
    
    Afterwards: ```Connect-Graph```
3. Run script via PowerShell dot sourcing
    
    ```& "C:\Users\$env:USERNAME\Documents\WindowsPowerShell\Scripts\Invoke-ConditionalAccessDocumentation.ps1"```
    
4. Pretty format the csv with excel & save it as excel workbook 

![Example](https://raw.githubusercontent.com/nicolonsky/ConditionalAccessDocumentation/master/Example/Example.png)

## Excel gimmicks
The following steps might help you to format the documentation.

1. Copy the CSV data to the clipboard
    ![Example](https://tech.nicolonsky.ch/content/images/2020/04/Annotation-2020-04-20-121447.png)

2. Create a new excel workbook

3. Right click & paste the csv data with the transpose option

    ![Example](https://tech.nicolonsky.ch/content/images/2020/04/Annotation-2020-04-20-121559.png)

4. Expand the rows and columns and ensure text wrap is turned on

    ![Example](https://tech.nicolonsky.ch/content/images/2020/04/image-4.png)

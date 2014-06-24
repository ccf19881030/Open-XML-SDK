Open-XML-SDK
============
The Open XML SDK provides open-source libraries for working with Open XML
Documents (DOCX, XLSX, and PPTX).  It supports scenarios such as:
- High-performance generation of word-processing documents, spreadsheets,
  and presentations
- Document modification, such as removing tracked revisions or removing
  unacceptable content from documents
- Data and content querying and extraction, such as transformation from
  DOCX to HTML, or extraction of data from spreadsheets

Copyright (c) Microsoft Open Technologies, Inc.  All rights reserved.
Licensed under the Apache License, Version 2.0.
See License.txt in the project root for license information.

Build Instructions
==================

Note: for this first release, you must have some version of Visual Studio
installed.  Visual Studio 2012 Express Edition will work just fine:
http://www.microsoft.com/en-us/download/details.aspx?id=34673

Set Execution Policy for PowerShell
===================================
In order to run the script that builds the Open XML SDK, you need to set
    the execution policy.  To set the execution policy, you must run
    PowerShell as administrator.
1.  Right click on the PowerShell shortcut, and click "Run as administrator".
    An easy way to find the PowerShell shortcut is to click the Start
    button, then type PowerShell.  The PowerShell shortcut will be in the
    search results above the start menu.
2.  Click the Yes button in the User Account Control dialog box.
3.  Run the command to set the execution policy:
    Type:
        PS C:\Windows\system32> Set-ExecutionPolicy Unrestricted<Enter>
4.  The Set-ExecutionPolicy cmdlet asks:
        Do you want to change the execution policy?
        [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
    Press <Enter>
5.  You can exit the PowerShell session that is running as administrator.
    Type:
        PS C:\Windows\system32> Exit<Enter>

Build the Open XML SDK Libraries
================================
1.  Start a Visual Studio command prompt.  It does not need to run as
    administrator.
2.  Change directories into the directory that contains this README.md,
    and the PowerShell script BldSdk.ps1
    For instance, type:
        C:> CD C:\users\<username>\Documents\Open-Xml-Sdk<Enter>
3.  Start PowerShell.
    Type:
        C:> PowerShell<Enter>
4.  Run the PowerShell script to build the libraries:
    Type:
        PS C:\users\Eric\Documents\Open-Xml-Sdk> ./BldSdk.ps1<Enter>
    The build will commence - it can take a few seconds, up to a minute,
    depending on the speed of your computer.
5.  Find the debug libraries in the folder: ./build/OpenXmlSdkLib/Debug
    Find the release libraries in the folder: ./build/OpenXmlSdkLib/Release
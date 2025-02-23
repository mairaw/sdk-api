---
UID: NF:msiquery.MsiCreateRecord
title: MsiCreateRecord function (msiquery.h)
description: The MsiCreateRecord function creates a new record object with the specified number of fields. This function returns a handle that should be closed using MsiCloseHandle.
old-location: setup\msicreaterecord.htm
tech.root: Msi
ms.assetid: fc1d5a09-3097-4a1c-a615-1b93f7eacb04
ms.date: 12/05/2018
ms.keywords: MsiCreateRecord, MsiCreateRecord function, _msi_msicreaterecord, msiquery/MsiCreateRecord, setup.msicreaterecord
f1_keywords:
- msiquery/MsiCreateRecord
dev_langs:
- c++
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Msi.dll
- Ext-MS-Win-MSI-Misc-l1-1-0.dll
api_name:
- MsiCreateRecord
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiCreateRecord function


## -description


The 
<b>MsiCreateRecord</b> function creates a new record object with the specified number of fields. This function returns a handle that should be closed using 
<a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>.


## -parameters




### -param cParams [in]

Specifies the number of fields the record will have. The maximum number of fields in a record is limited to 65535.


## -returns



If the function succeeds, the return value is handle to a new record object.

If the function fails, the return value is null.




## -remarks



Field 0 of the record object created by the 
<b>MsiCreateRecord</b> function is used for format strings and operation codes and is not included in the count specified by <i>cParams</i>. All fields are initialized to null.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>. For more information see <a href="https://docs.microsoft.com/windows/desktop/Msi/windows-installer-best-practices">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="https://docs.microsoft.com/windows/desktop/Msi/windows-installer-best-practices">Windows Installer Best Practices</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Database Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Record Processing Functions</a>
 

 


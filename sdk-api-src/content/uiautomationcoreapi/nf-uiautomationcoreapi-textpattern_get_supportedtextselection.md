---
UID: NF:uiautomationcoreapi.TextPattern_get_SupportedTextSelection
title: TextPattern_get_SupportedTextSelection function (uiautomationcoreapi.h)
description: Ascertains whether the text container's contents can be selected and deselected.
old-location: winauto\uiauto_TextPattern_get_SupportedTextSelectionConPat.htm
tech.root: WinAuto
ms.assetid: d938197b-9500-4744-a0d7-0d0ac5dd58b9
ms.date: 12/05/2018
ms.keywords: TextPattern_get_SupportedTextSelection, TextPattern_get_SupportedTextSelection function [Windows Accessibility], uiauto.uiauto_TextPattern_get_SupportedTextSelectionConPat, uiauto_TextPattern_get_SupportedTextSelectionConPat, uiautomationcoreapi/TextPattern_get_SupportedTextSelection, winauto.uiauto_TextPattern_get_SupportedTextSelectionConPat
f1_keywords:
- uiautomationcoreapi/TextPattern_get_SupportedTextSelection
dev_langs:
- c++
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Uiautomationcore.dll
api_name:
- TextPattern_get_SupportedTextSelection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TextPattern_get_SupportedTextSelection function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Ascertains whether the text container's contents can be selected and deselected.


## -parameters




### -param hobj [in]

Type: <b>HUIAPATTERNOBJECT</b>

A control pattern object.


### -param pRetVal [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

When this function returns, contains a value indicating whether the text 
				container can have its contents selected and deselected. 
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




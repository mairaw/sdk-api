---
UID: NF:ole.OleLoadFromStream
title: OleLoadFromStream function (ole.h)
description: Loads an object from the stream.
old-location: com\oleloadfromstream.htm
tech.root: com
ms.assetid: 2d54a0ef-906b-4886-a095-4ff2f3d4e634
ms.date: 12/05/2018
ms.keywords: OleLoadFromStream, OleLoadFromStream function [COM], _ole_OleLoadFromStream, com.oleloadfromstream, ole/OleLoadFromStream
f1_keywords:
- ole/OleLoadFromStream
dev_langs:
- c++
req.header: ole.h
req.include-header: Ole2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ole32.dll
- Ext-MS-Win-OLE32-IE-Ext-l1-1-0.dll
api_name:
- OleLoadFromStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# OleLoadFromStream function


## -description


Loads an object from the stream.


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD


### -param arg4

TBD


### -param arg5

TBD


### -param arg6

TBD




#### - iidInterface [in]

Interface identifier (IID) the caller wants to use to communicate with the object after it is loaded.


#### - pStm [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream</a> interface on the stream from which the object is to be loaded.


#### - ppvObj [out]

Address of pointer variable that receives the interface pointer requested in riid. Upon successful return, *<i>ppvObj</i> contains the requested interface pointer on the newly loaded object.


## -returns



This function returns S_OK on success. Other possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the specified interface.

</td>
</tr>
</table>
 

This function can also return any of the error values returned by the <a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-readclassstm">ReadClassStm</a> and <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> functions, and the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-ipersiststream-load">IPersistStream::Load</a> method.




## -remarks



<div class="alert"><b>Important</b>  <p class="note">Security Note: Calling this method with untrusted data is a security risk. Call this method only with trusted data. For more information, see <a href="http://go.microsoft.com/fwlink/?LinkId=798821">Untrusted Data Security Risks</a>.

</div>
<div> </div>
This function can be used to load an object that supports the <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> interface. The CLSID of the object must immediately precede the object's data in the stream, which is accomplished by the companion function <a href="https://docs.microsoft.com/windows/desktop/api/ole/nf-ole-olesavetostream">OleSaveToStream</a> (or the operations it wraps, which are described under that topic).



If the CLSID for the stream is CLSID_NULL, the <i>ppvObj</i> parameter is set to <b>NULL</b>.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ole/nf-ole-olesavetostream">OleSaveToStream</a>
 

 


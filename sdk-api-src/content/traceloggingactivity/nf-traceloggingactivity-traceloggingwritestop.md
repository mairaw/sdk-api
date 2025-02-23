---
UID: NF:traceloggingactivity.TraceLoggingWriteStop
title: TraceLoggingWriteStop macro (traceloggingactivity.h)
description: Stops an activity and logs the stop event.
old-location: tracelogging\traceloggingwritestop.htm
tech.root: tracelogging
ms.assetid: 638F08E3-5970-40B3-8025-E3D81ECA1D2A
ms.date: 12/05/2018
ms.keywords: TraceLoggingWriteStop, TraceLoggingWriteStop macro, tracelogging.traceloggingwritestop, traceloggingactivity/TraceLoggingWriteStop
f1_keywords:
- traceloggingactivity/TraceLoggingWriteStart
dev_langs:
- c++
req.header: traceloggingactivity.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2012 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- traceloggingactivity.h
api_name:
- TraceLoggingWriteStart
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TraceLoggingWriteStop macro


## -description


Stops an activity and logs the stop event.

The activity must not have already been stopped.


## -parameters




### -param activity [in]

The activity to start.


### -param name [in]

The name of the event. This must be a string literal and not a variable. It cannot have any embedded nul characters.


#### - args [in, optional]

Additional parameters added to the event. The maximum number of optional parameters is 99. All parameters must be wrapper macros as defined in <a href="https://docs.microsoft.com/windows/desktop/tracelogging/tracelogging-wrapper-macros">TraceLogging Wrapper Macros</a>.

The args should not include <b>TraceLoggingLevel</b>, <b>TraceLoggingKeyword</b>, or <b>TraceLoggingOpcode</b>. The level and keyword are set on the activity itself, and the opcode for a stop event is always “Stop”.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart">TraceLoggingWriteStart</a>
 

 


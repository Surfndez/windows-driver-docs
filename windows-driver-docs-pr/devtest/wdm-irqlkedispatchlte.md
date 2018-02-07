---
title: IrqlKeDispatchLte rule (wdm)
ms.assetid: 425a20ea-c9e3-45f4-a517-6bad9ab0de98
description: 
keywords: ["IrqlKeDispatchLte rule (wdm)"]
topic_type:
- apiref
api_name:
- IrqlKeDispatchLte
api_type:
- NA
---

# IrqlKeDispatchLte rule (wdm)


The **IrqlKeDispatchLte** rule specifies that the driver calls the following kernel routines only when it is executing at IRQL &lt;= DISPATCH\_LEVEL:

-   [**KeAcquireSpinLock**](https://msdn.microsoft.com/library/windows/hardware/ff551917)

-   [**KeCancelTimer**](https://msdn.microsoft.com/library/windows/hardware/ff551970)

-   [**KeClearEvent**](https://msdn.microsoft.com/library/windows/hardware/ff551980)

-   [**KeFlushIoBuffers**](https://msdn.microsoft.com/library/windows/hardware/ff552041)

-   [**KeInitializeDeviceQueue**](https://msdn.microsoft.com/library/windows/hardware/ff552126)

-   [**KeInitializeTimer**](https://msdn.microsoft.com/library/windows/hardware/ff552168)

-   [**KeInitializeTimerEx**](https://msdn.microsoft.com/library/windows/hardware/ff552173)

-   [**KePulseEvent**](https://msdn.microsoft.com/library/windows/hardware/ff552979)

-   [**KeRaiseIrqlToDpcLevel**](https://msdn.microsoft.com/library/windows/hardware/ff553084)

-   [**KeReadStateEvent**](https://msdn.microsoft.com/library/windows/hardware/ff553089)

-   [**KeReadStateTimer**](https://msdn.microsoft.com/library/windows/hardware/ff553099)

-   [**KeReleaseMutex**](https://msdn.microsoft.com/library/windows/hardware/ff553140)

-   [**KeRemoveEntryDeviceQueue**](https://msdn.microsoft.com/library/windows/hardware/ff553163)

-   [**KeResetEvent**](https://msdn.microsoft.com/library/windows/hardware/ff553176)

-   [**KeSaveFloatingPointState**](https://msdn.microsoft.com/library/windows/hardware/ff553243)

-   [**KeSetTimer**](https://msdn.microsoft.com/library/windows/hardware/ff553286)

-   [**KeSetTimerEx**](https://msdn.microsoft.com/library/windows/hardware/ff553292)

|              |     |
|--------------|-----|
| Driver model | WDM |

|                                   |                                                                                                                                       |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Bug check(s) found with this rule | [**Bug Check 0xC4: DRIVER\_VERIFIER\_DETECTED\_VIOLATION**](https://msdn.microsoft.com/library/windows/hardware/ff560187) (0x00020011) |

How to test
-----------

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">At compile time</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Run [Static Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff552808) and specify the <strong>IrqlKeDispatchLte</strong> rule.</p>
Use the following steps to run an analysis of your code:
<ol>
<li>[Prepare your code (use role type declarations).](https://msdn.microsoft.com/library/windows/hardware/hh454281#preparing-your-source-code)</li>
<li>[Run Static Driver Verifier.](https://msdn.microsoft.com/library/windows/hardware/hh454281#running-static-driver-verifier)</li>
<li>[View and analyze the results.](https://msdn.microsoft.com/library/windows/hardware/hh454281#viewing-and-analyzing-the-results)</li>
</ol>
<p>For more information, see [Using Static Driver Verifier to Find Defects in Drivers](https://msdn.microsoft.com/library/windows/hardware/hh454281).</p></td>
</tr>
</tbody>
</table>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">At run time</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Run [Driver Verifier](https://msdn.microsoft.com/library/windows/hardware/ff545448) and select the [DDI compliance checking](https://msdn.microsoft.com/library/windows/hardware/hh454208) option.</p></td>
</tr>
</tbody>
</table>

 

Applies to
----------

[**KeAcquireSpinLock**](https://msdn.microsoft.com/library/windows/hardware/ff551917)
[**KeCancelTimer**](https://msdn.microsoft.com/library/windows/hardware/ff551970)
[**KeClearEvent**](https://msdn.microsoft.com/library/windows/hardware/ff551980)
[**KeInitializeDeviceQueue**](https://msdn.microsoft.com/library/windows/hardware/ff552126)
[**KeInitializeSemaphore**](https://msdn.microsoft.com/library/windows/hardware/ff552150)
[**KeInitializeTimer**](https://msdn.microsoft.com/library/windows/hardware/ff552168)
[**KeInitializeTimerEx**](https://msdn.microsoft.com/library/windows/hardware/ff552173)
[**KePulseEvent**](https://msdn.microsoft.com/library/windows/hardware/ff552979)
[**KeReadStateEvent**](https://msdn.microsoft.com/library/windows/hardware/ff553089)
[**KeReadStateTimer**](https://msdn.microsoft.com/library/windows/hardware/ff553099)
[**KeReleaseMutex**](https://msdn.microsoft.com/library/windows/hardware/ff553140)
[**KeRemoveEntryDeviceQueue**](https://msdn.microsoft.com/library/windows/hardware/ff553163)
[**KeResetEvent**](https://msdn.microsoft.com/library/windows/hardware/ff553176)
[**KeSaveFloatingPointState**](https://msdn.microsoft.com/library/windows/hardware/ff553243)
[**KeSetTimer**](https://msdn.microsoft.com/library/windows/hardware/ff553286)
[**KeSetTimerEx**](https://msdn.microsoft.com/library/windows/hardware/ff553292)
 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevtest\devtest%5D:%20IrqlKeDispatchLte%20rule%20%28wdm%29%20%20RELEASE:%20%281/17/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")




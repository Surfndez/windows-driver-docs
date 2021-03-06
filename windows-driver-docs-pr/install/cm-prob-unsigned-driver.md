---
title: CM_PROB_UNSIGNED_DRIVER
description: CM_PROB_UNSIGNED_DRIVER
ms.assetid: 91d37d25-ca0d-413f-9e6f-5a22a0406714
ms.date: 04/20/2017
ms.localizationpriority: medium
---

# CM_PROB_UNSIGNED_DRIVER

This function is reserved for system use.

The device did not start on a 64-bit version of Windows because it has a driver that is not digitally signed. For more information about how to sign drivers, see [Driver Signing](driver-signing.md).

## Error

52

### Display Message

"Windows cannot verify the digital signature for the drivers required for this device. A recent hardware or software change might have installed a file that is signed incorrectly or damaged, or that might be malicious software from an unknown source. (Code 52)"

### Recommended Resolution

The driver does not comply with the [kernel-mode code signing policy](kernel-mode-code-signing-policy--windows-vista-and-later-.md).

For end-users, the only way to avoid this error is to obtain and install a digitally signed driver for the device.

For driver developers, you can use various methods to load an unsigned driver on a 64-bit version of Windows. For more information, see [Installing an Unsigned Driver during Development and Test](installing-an-unsigned-driver-during-development-and-test.md).

## See Also

[Code Integrity Diagnostic System Log Events](https://docs.microsoft.com/windows-hardware/drivers/install/code-integrity-diagnostic-system-log-events)

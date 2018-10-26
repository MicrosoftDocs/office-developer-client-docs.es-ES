---
title: Determinar si Outlook descarga solo el encabezado de un mensaje
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: acc96bb9-1592-c480-53ee-1325f65297e1
description: 'Última modificación: 25 de junio de 2012'
ms.openlocfilehash: 1240faddf2ebc8b645b6c6bde6aba243e9019507
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563565"
---
# <a name="determine-if-outlook-downloaded-only-the-header-of-a-message"></a><span data-ttu-id="7bf40-103">Determinar si Outlook descarga solo el encabezado de un mensaje</span><span class="sxs-lookup"><span data-stu-id="7bf40-103">Determine if Outlook downloaded only the header of a message</span></span>

<span data-ttu-id="7bf40-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bf40-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bf40-105">En este tema se muestra un ejemplo de código en Visual C++ que usa la con nombre [Canónico de PidLidHeaderItem (propiedad)](pidlidheaderitem-canonical-property.md) para determinar si ha descargado Microsoft Outlook 2013 sólo el encabezado de un mensaje o el encabezado y el cuerpo de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="7bf40-105">This topic shows a code sample in Visual C++ that uses the named [PidLidHeaderItem Canonical Property](pidlidheaderitem-canonical-property.md) to determine whether Microsoft Outlook 2013 has downloaded only the header of a message or the header and the body of a message.</span></span> 
  
```cpp
BOOL bIsHeader(LPMESSAGE lpMessage) 
{ 
    HRESULT         hRes = S_OK; 
    BOOL            bRet = false; 
    ULONG    ulVal = 0; 
    LPSPropValue    lpPropVal = NULL; 
    LPSPropTagArray lpNamedPropTag = NULL; 
    MAPINAMEID      NamedID = {0}; 
    LPMAPINAMEID    lpNamedID = NULL; 
 
    NamedID.lpguid = (LPGUID) &PSETID_Common; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidHeaderItem; 
    lpNamedID = &NamedID; 
    hRes = lpMessage->GetIDsFromNames(1, &lpNamedID, NULL, &lpNamedPropTag); 
 
    if (lpNamedPropTag && 1 == lpNamedPropTag->cValues) 
    { 
lpNamedPropTag->aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTag->aulPropTag[0], PT_LONG); 
 
//Get the value of the property. 
hRes = lpMessage->GetProps(lpNamedPropTag, 0, &ulVal, &lpPropVal); 
if (lpPropVal && 1 == ulVal && PT_LONG == PROP_TYPE(lpPropVal->ulPropTag) && lpPropVal->Value.ul) 
{ 
    bRet = true; 
} 
    } 
 
    MAPIFreeBuffer(lpPropVal); 
    MAPIFreeBuffer(lpNamedPropTag); 
    return bRet; 
}

```



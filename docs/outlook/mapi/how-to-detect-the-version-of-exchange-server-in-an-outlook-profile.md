---
title: Detectar la versión de Exchange Server en un perfil de Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: c6aaac128e1a3e1a8d77d3fa8b6c50a335348b71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424451"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a>Detectar la versión de Exchange Server en un perfil de Outlook

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
En este tema se incluye un ejemplo de código en C++ que muestra cómo usar la propiedad **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** y la propiedad **[PR_PROFILE_SERVER_FULL_VERSION para](pidtagprofileserverfullversion-canonical-property.md)** obtener información de versión del Microsoft Exchange Server al que está conectada la cuenta activa. 
  
La  `GetProfileServiceVersion` función del ejemplo de código acepta un perfil como parámetro de entrada. Según si la **propiedad PR_PROFILE_SERVER_VERSION** y la propiedad **PR_PROFILE_SERVER_FULL_VERSION** existen en el perfil determinado, la función obtiene cada propiedad y devuelve la información de versión adecuada como parámetros de salida. 
  
`GetProfileServiceVersion` primero llama a la **[función MAPIAdminProfiles](mapiadminprofiles.md)** para crear un objeto de administración de perfiles. A continuación, usa el objeto de administración de perfiles para llamar a **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** para obtener un objeto de administración del servicio de mensajes. Con el objeto de administración del servicio de mensajes, llama a **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** para obtener una sección del perfil actual y, a continuación, llama a **[HrGetOneProp](hrgetoneprop.md)** para comprobar si cada una de las dos propiedades existe en esa sección del perfil y, si es así, establece la información de versión en los parámetros de salida adecuados. 
  
```cpp
TZDEFINITION* BinToTZDEFINITION(ULONG cbDef, LPBYTE lpbDef) 
{ 
    if (!lpbDef) return NULL; 
 
    // Update this if parsing code is changed. 
    // This checks the size up to the flag member. 
    if (cbDef &lt; 2*sizeof(BYTE) + 2*sizeof(WORD)) return NULL; 
 
    TZDEFINITION tzDef = {0}; 
    TZRULE* lpRules = NULL; 
    LPBYTE lpPtr = lpbDef; 
    WORD cchKeyName = NULL; 
    WCHAR* szKeyName = NULL; 
    WORD i = 0; 
 
    BYTE bMajorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
    BYTE bMinorVersion = *((BYTE*)lpPtr); 
    lpPtr += sizeof(BYTE); 
 
    // We only understand TZ_BIN_VERSION_MAJOR 
    if (TZ_BIN_VERSION_MAJOR != bMajorVersion) return NULL; 
 
    // We only understand if &gt;= TZ_BIN_VERSION_MINOR 
    if (TZ_BIN_VERSION_MINOR &gt; bMinorVersion) return NULL; 
 
    lpPtr += sizeof(WORD); 
 
    tzDef.wFlags = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
 
    if (TZDEFINITION_FLAG_VALID_GUID &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(GUID)) return NULL; 
        tzDef.guidTZID = *((GUID*)lpPtr); 
        lpPtr += sizeof(GUID); 
    } 
 
    if (TZDEFINITION_FLAG_VALID_KEYNAME &amp; tzDef.wFlags) 
    { 
        if (lpbDef + cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
        cchKeyName = *((WORD*)lpPtr); 
        lpPtr += sizeof(WORD); 
        if (cchKeyName) 
        { 
            if (lpbDef + cbDef - lpPtr &lt; (BYTE)sizeof(WORD)*cchKeyName) return NULL; 
            szKeyName = (WCHAR*)lpPtr; 
            lpPtr += cchKeyName*sizeof(WORD); 
        } 
    } 
 
    if (lpbDef+ cbDef - lpPtr &lt; sizeof(WORD)) return NULL; 
    tzDef.cRules = *((WORD*)lpPtr); 
    lpPtr += sizeof(WORD); 
    if (tzDef.cRules) 
    { 
        lpRules = new TZRULE[tzDef.cRules]; 
        if (!lpRules) return NULL; 
 
        LPBYTE lpNextRule = lpPtr; 
        BOOL bRuleOK = false; 

```



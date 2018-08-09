---
title: Detectar la versión de Exchange Server en un perfil de Outlook
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e2d8d8a9-7e8f-9cf0-56a8-d8a6281ad589
description: 'Última modificación: 03 de julio de 2012'
ms.openlocfilehash: 3ed3def3fd76ec4f67239958b5d5164d97f81d8d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816972"
---
# <a name="detect-the-version-of-exchange-server-in-an-outlook-profile"></a>Detectar la versión de Exchange Server en un perfil de Outlook

**Hace referencia a**: Outlook 
  
En este tema se incluye un ejemplo de código en C++ que se muestra cómo usar la propiedad **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** y **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** (propiedad) para obtener información de la versión de Microsoft Exchange Server que es la cuenta de activada conectado a. 
  
El `GetProfileServiceVersion` función en el ejemplo de código acepta un perfil como un parámetro de entrada. Dependiendo de si la propiedad **PR_PROFILE_SERVER_VERSION** y la propiedad **PR_PROFILE_SERVER_FULL_VERSION** existen en el perfil dado, la función obtiene cada propiedad y devuelve la información de versión adecuada como resultado parámetros. 
  
`GetProfileServiceVersion`en primer lugar llama a la función **[MAPIAdminProfiles](mapiadminprofiles.md)** para crear un objeto de administración de perfiles. A continuación, se utiliza el objeto de administración de perfiles para llamar a **[IProfAdmin::AdminServices](iprofadmin-adminservices.md)** para obtener un objeto de administración del servicio de mensajes. Uso del objeto de administración de servicio de mensaje, se llama a **[IMsgServiceAdmin::OpenProfileSection](imsgserviceadmin-openprofilesection.md)** para obtener una sección del perfil actual y, a continuación, llama a **[HrGetOneProp](hrgetoneprop.md)** para comprobar si cada una de las dos propiedades existe en esa sección de la perfiles y, si es así, se establece la información de versión en los parámetros de salida correspondiente. 
  
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



---
title: Obtener un mensaje de contacto determinado en una entrada de la libreta de direcciones de contactos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Última modificación: 13 de agosto de 2013'
ms.openlocfilehash: 472b5847053c0a18026c76b8055a26551331d8dd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564545"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a>Obtener un mensaje de contacto determinado en una entrada de la libreta de direcciones de contactos

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema contiene un ejemplo en C++, `HrOpenContact`, que muestra cómo usar la estructura [CONTAB_ENTRYID](contab_entryid.md) que identifica una entrada en una libreta de direcciones de contactos para obtener el mensaje MAPI contacto asociado. 
  
`HrOpenContact`tiene los siguientes parámetros: 
  
-  *lpSession* es un parámetro de entrada que representa la sesión actual. **LPMAPISESSION** se define en el mapix.h de archivo de encabezado MAPI como un puntero a [IMAPISession: IUnknown](imapisessioniunknown.md).
    
-  *cbEntryID* es un parámetro de entrada que representa el tamaño del identificador de entrada asociado con *lpEntryID* . 
    
-  *lpEntryID* es un parámetro de entrada que representa un puntero al identificador de entrada de una entrada de un contacto de la libreta de direcciones. 
    
-  *ulFlags* es un parámetro de entrada que representa una máscara de bits que contiene los indicadores de objeto de acceso al mensaje de contacto de MAPI. 
    
-  *lpContactMessage* es un parámetro de salida que representa un puntero al mensaje de contacto de MAPI. 
    
Para abrir el mensaje de contacto de MAPI subyacente, `HrOpenContact` en primer lugar convierte *lpEntryID* a un puntero a **CONTAB_ENTRYID**. A continuación, llama a [IMAPISession::OpenEntry](imapisession-openentry.md) para obtener el mensaje de contacto de MAPI, pasando como parámetros los campos *cbeid* y *abeid* de la entrada en la libreta de direcciones de contactos que identifican, respectivamente, el tamaño del identificador de entrada y el identificador de entrada del mensaje de contacto de MAPI. 
  
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

## <a name="see-also"></a>Recursos adicionales

- [IMAPISession::OpenEntry](imapisession-openentry.md)


---
title: Obtener un mensaje de contacto determinado en una entrada de la libreta de direcciones de contactos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Última modificación: 13 de agosto de 2013'
ms.openlocfilehash: 346e6bc471f5257aacb34c2e7d02a0aade1bb46e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816995"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a><span data-ttu-id="06ab5-103">Obtener un mensaje de contacto determinado en una entrada de la libreta de direcciones de contactos</span><span class="sxs-lookup"><span data-stu-id="06ab5-103">Obtain a contact message given a contacts address book entry</span></span>

<span data-ttu-id="06ab5-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="06ab5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="06ab5-105">Este tema contiene un ejemplo en C++, `HrOpenContact`, que muestra cómo usar la estructura [CONTAB_ENTRYID](contab_entryid.md) que identifica una entrada en una libreta de direcciones de contactos para obtener el mensaje MAPI contacto asociado.</span><span class="sxs-lookup"><span data-stu-id="06ab5-105">This topic contains an example in C++, `HrOpenContact`, that shows how to use the [CONTAB_ENTRYID](contab_entryid.md) structure that identifies an entry in a Contacts Address Book to obtain the associated MAPI Contact message.</span></span> 
  
<span data-ttu-id="06ab5-106">`HrOpenContact`tiene los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="06ab5-106">`HrOpenContact` has the following parameters:</span></span> 
  
-  <span data-ttu-id="06ab5-107">*lpSession* es un parámetro de entrada que representa la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="06ab5-107">*lpSession*  is an input parameter representing the current session.</span></span> <span data-ttu-id="06ab5-108">**LPMAPISESSION** se define en el mapix.h de archivo de encabezado MAPI como un puntero a [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="06ab5-108">**LPMAPISESSION** is defined in the MAPI header file mapix.h as a pointer to [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span>
    
-  <span data-ttu-id="06ab5-109">*cbEntryID* es un parámetro de entrada que representa el tamaño del identificador de entrada asociado con *lpEntryID* .</span><span class="sxs-lookup"><span data-stu-id="06ab5-109">*cbEntryID*  is an input parameter representing the size of the entry identifier associated with  *lpEntryID*  .</span></span> 
    
-  <span data-ttu-id="06ab5-110">*lpEntryID* es un parámetro de entrada que representa un puntero al identificador de entrada de una entrada de un contacto de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="06ab5-110">*lpEntryID*  is an input parameter representing a pointer to the entry identifier of an entry in a Contact Address Book.</span></span> 
    
-  <span data-ttu-id="06ab5-111">*ulFlags* es un parámetro de entrada que representa una máscara de bits que contiene los indicadores de objeto de acceso al mensaje de contacto de MAPI.</span><span class="sxs-lookup"><span data-stu-id="06ab5-111">*ulFlags*  is an input parameter representing a bitmask containing object access flags to the MAPI Contact message.</span></span> 
    
-  <span data-ttu-id="06ab5-112">*lpContactMessage* es un parámetro de salida que representa un puntero al mensaje de contacto de MAPI.</span><span class="sxs-lookup"><span data-stu-id="06ab5-112">*lpContactMessage*  is an output parameter representing a pointer to the MAPI Contact message.</span></span> 
    
<span data-ttu-id="06ab5-113">Para abrir el mensaje de contacto de MAPI subyacente, `HrOpenContact` en primer lugar convierte *lpEntryID* a un puntero a **CONTAB_ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="06ab5-113">To open the underlying MAPI Contact message,  `HrOpenContact` first casts  *lpEntryID*  to a pointer to **CONTAB_ENTRYID**.</span></span> <span data-ttu-id="06ab5-114">A continuación, llama a [IMAPISession::OpenEntry](imapisession-openentry.md) para obtener el mensaje de contacto de MAPI, pasando como parámetros los campos *cbeid* y *abeid* de la entrada en la libreta de direcciones de contactos que identifican, respectivamente, el tamaño del identificador de entrada y el identificador de entrada del mensaje de contacto de MAPI.</span><span class="sxs-lookup"><span data-stu-id="06ab5-114">It then calls [IMAPISession::OpenEntry](imapisession-openentry.md) to obtain the MAPI Contact message, passing as parameters the  *cbeid*  and  *abeid*  fields of the entry in the Contacts Address Book that identify respectively the size of the entry identifier and the entry identifier of the MAPI Contact message.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="06ab5-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="06ab5-115">See also</span></span>

- [<span data-ttu-id="06ab5-116">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="06ab5-116">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)


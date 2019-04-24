---
title: Obtener un mensaje de contacto según una entrada de la libreta de direcciones de contactos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a263894b-b3da-f1e4-a7da-ca3695bddc94
description: 'Última modificación: 13 de agosto de 2013'
ms.openlocfilehash: be988a3036c2d882f65e2e588cc9a40bfda146a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345960"
---
# <a name="obtain-a-contact-message-given-a-contacts-address-book-entry"></a><span data-ttu-id="47eed-103">Obtener un mensaje de contacto según una entrada de la libreta de direcciones de contactos</span><span class="sxs-lookup"><span data-stu-id="47eed-103">Obtain a contact message given a contacts address book entry</span></span>

<span data-ttu-id="47eed-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47eed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47eed-105">Este tema contiene un ejemplo de C++, `HrOpenContact`que muestra cómo usar la estructura [CONTAB_ENTRYID](contab_entryid.md) que identifica una entrada en una libreta de direcciones de contactos para obtener el mensaje de contacto MAPI asociado.</span><span class="sxs-lookup"><span data-stu-id="47eed-105">This topic contains an example in C++, `HrOpenContact`, that shows how to use the [CONTAB_ENTRYID](contab_entryid.md) structure that identifies an entry in a Contacts Address Book to obtain the associated MAPI Contact message.</span></span> 
  
<span data-ttu-id="47eed-106">`HrOpenContact`tiene los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="47eed-106">`HrOpenContact` has the following parameters:</span></span> 
  
-  <span data-ttu-id="47eed-107">*lpSession* es un parámetro de entrada que representa la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="47eed-107">*lpSession*  is an input parameter representing the current session.</span></span> <span data-ttu-id="47eed-108">**LPMAPISESSION** se define en el archivo de encabezado MAPI mapix. h como un puntero a [IMAPISession: IUnknown](imapisessioniunknown.md).</span><span class="sxs-lookup"><span data-stu-id="47eed-108">**LPMAPISESSION** is defined in the MAPI header file mapix.h as a pointer to [IMAPISession : IUnknown](imapisessioniunknown.md).</span></span>
    
-  <span data-ttu-id="47eed-109">*cbEntryID* es un parámetro de entrada que representa el tamaño del identificador de entrada asociado a *lpEntryID* .</span><span class="sxs-lookup"><span data-stu-id="47eed-109">*cbEntryID*  is an input parameter representing the size of the entry identifier associated with  *lpEntryID*  .</span></span> 
    
-  <span data-ttu-id="47eed-110">*lpEntryID* es un parámetro de entrada que representa un puntero al identificador de entrada de una entrada en una libreta de direcciones de contacto.</span><span class="sxs-lookup"><span data-stu-id="47eed-110">*lpEntryID*  is an input parameter representing a pointer to the entry identifier of an entry in a Contact Address Book.</span></span> 
    
-  <span data-ttu-id="47eed-111">*ulFlags* es un parámetro de entrada que representa una máscara de datos que contiene indicadores de acceso a objetos al mensaje de contacto MAPI.</span><span class="sxs-lookup"><span data-stu-id="47eed-111">*ulFlags*  is an input parameter representing a bitmask containing object access flags to the MAPI Contact message.</span></span> 
    
-  <span data-ttu-id="47eed-112">*lpContactMessage* es un parámetro de salida que representa un puntero al mensaje de contacto de MAPI.</span><span class="sxs-lookup"><span data-stu-id="47eed-112">*lpContactMessage*  is an output parameter representing a pointer to the MAPI Contact message.</span></span> 
    
<span data-ttu-id="47eed-113">Para abrir el mensaje de contacto MAPI subyacente `HrOpenContact` , primero convierte *lpEntryID* en un puntero a **CONTAB_ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="47eed-113">To open the underlying MAPI Contact message,  `HrOpenContact` first casts  *lpEntryID*  to a pointer to **CONTAB_ENTRYID**.</span></span> <span data-ttu-id="47eed-114">A continuación, llama a [IMAPISession:: OpenEntry](imapisession-openentry.md) para obtener el mensaje de contacto de MAPI, pasando como parámetros los campos *cbeid* y *Abeid* de la entrada de la libreta de direcciones Contacts que identifican respectivamente el tamaño del identificador de entrada y el identificador de entrada del mensaje de contacto de MAPI.</span><span class="sxs-lookup"><span data-stu-id="47eed-114">It then calls [IMAPISession::OpenEntry](imapisession-openentry.md) to obtain the MAPI Contact message, passing as parameters the  *cbeid*  and  *abeid*  fields of the entry in the Contacts Address Book that identify respectively the size of the entry identifier and the entry identifier of the MAPI Contact message.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="47eed-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="47eed-115">See also</span></span>

- [<span data-ttu-id="47eed-116">IMAPISession::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="47eed-116">IMAPISession::OpenEntry</span></span>](imapisession-openentry.md)


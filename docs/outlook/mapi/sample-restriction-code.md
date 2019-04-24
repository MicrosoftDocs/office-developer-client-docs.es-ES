---
title: Código de restricción de muestra
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9b82097c-dbd6-4ba0-a6cb-292301f9402b
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: cafcb20cbce3019d7623d330721005a674eca36e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314948"
---
# <a name="sample-restriction-code"></a><span data-ttu-id="c329c-103">Código de restricción de muestra</span><span class="sxs-lookup"><span data-stu-id="c329c-103">Sample restriction code</span></span>

<span data-ttu-id="c329c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c329c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c329c-105">El código de ejemplo siguiente muestra cómo crear una restricción que filtre todos los mensajes que no contengan la palabra "Volleyball" en la línea de asunto y que no se hayan enviado a Sue desde Sam.</span><span class="sxs-lookup"><span data-stu-id="c329c-105">The following sample code shows how to create a restriction that filters out all messages that do not contain the word "volleyball" in the subject line and were not sent to Sue from Sam.</span></span> <span data-ttu-id="c329c-106">Se requiere un árbol de estructuras [SRestriction](srestriction.md) , donde el nodo superior es una restricción **and** que se implementa con una estructura [SAndRestriction](sandrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="c329c-106">A tree of [SRestriction](srestriction.md) structures is required, with the top node being an **AND** restriction implemented with an [SAndRestriction](sandrestriction.md) structure.</span></span> <span data-ttu-id="c329c-107">Las tres restricciones que se unen mediante la operación **and** son una restricción de subobjeto que busca los mensajes enviados a Sue, una restricción de contenido que busca mensajes de Sam y otro **y** una restricción que busca mensajes que tienen un asunto que contiene "Volleyball".</span><span class="sxs-lookup"><span data-stu-id="c329c-107">The three restrictions that are joined by the **AND** operation are a subobject restriction that searches for messages sent to Sue, a content restriction that searches for messages from Sam, and another **AND** restriction that searches for messages that have a subject containing "volleyball."</span></span> <span data-ttu-id="c329c-108">Debido a que **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) no es una propiedad obligatoria, debe incluirse una restricción **exist** .</span><span class="sxs-lookup"><span data-stu-id="c329c-108">Because **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) is not a required property, an **Exist** restriction must be included.</span></span> 
  
<span data-ttu-id="c329c-109">Este código utiliza la asignación e inicialización dinámicas; también es posible asignar e inicializar de forma estática.</span><span class="sxs-lookup"><span data-stu-id="c329c-109">This code uses dynamic allocation and initialization; it is possible to allocate and initialize statically as well.</span></span> <span data-ttu-id="c329c-110">En aras de la brevedad, la comprobación de errores que debe producirse después de las llamadas de asignación no se incluye en el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c329c-110">In the interest of brevity, the error checking that must occur following the allocation calls is not included in the sample.</span></span> 
  
```cpp
HRESULT BuildRestriction (LPSTR pszSent, LPSTR pszFrom,
                                LPSTR pszSubjectText);
{
    LPSRestriction pRest, pAndRes, pObjRes, pSubjAndRes;
    LPSPropValue pRecip, pSender, pSubject;
    HRESULT hResult;
    ULONG ulResCount = 3, ulSubjCount = 2
    // Allocate and build  restriction to join criteria
    hResult = MAPIAllocateMore (sizeof(SRestriction)*ulResCount, pRest,
            (LPVOID *)&pAndRes);
    pRest->rt = RES_AND;
    pRest->res.resAnd.cRes = ulResCount;
    pRest->res.resAnd.lpRes = pAndRes;
    // Allocate and build subobject restriction to search recipient list
    hResult = MAPIAllocateMore (sizeof(SRestriction), pRest,
            (LPVOID *)&pObjRes);
    pAndRes[0].rt = RES_SUBRESTRICTION;
    pAndRes[0].res.resSub.ulSubObject = PR_MESSAGE_RECIPIENTS;
    pAndRes[0].res.resSub.lpRes = pObjRes;
    // Allocate and build content restriction to look for recipient
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pRecip);
    pObjRes->rt = RES_CONTENT;
    pObjRes->res.resContent.ulFuzzyLevel =
            FL_FULLSTRING | FL_IGNORECASE;
    pObjRes->res.resContent.ulPropTag = pRecip->ulPropTag =
            PR_DISPLAY_NAME;
    pObjRes->res.resContent.lpProp = pRecip;
    pRecip->Value.LPSZ = pszSent;              // pszSent set to Sue
    // Allocate and build content restriction to look for sender
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSend);
    pAndRes[1].rt = RES_CONTENT;
    pAndRes[1].res.resContent.ulFuzzyLevel =
            FL_FULLSTRING | FL_IGNORECASE;
    pAndRes[1].res.resContent.ulPropTag = pSend->ulPropTag =
            PR_SENDER_NAME;
    pAndRes[1].res.resContent.lpProp = pSend;
    pSend->Value.LPSZ = pszName;                    // pszName set to Sam
    // Allocate and build  restriction to look for subject
    hResult = MAPIAllocateMore (sizeof(SRestriction)*ulSubjCount, pRest,
            (LPVOID *)&pSubjAndRes);
    pRest->rt = RES_AND;
    pRest->res.resAnd.cRes = ulResCount;
    pRest->res.resAnd.lpRes = pAndRes;
    // Create an  restriction to search for subject
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubjAndRes);
    pAndRes[2].rt = RES_AND;
    pAndRes[2].res.resAnd.cRes = ulSubjCount;
    pAndRes[2].res.resAnd.lpRes = pSubjAndRes;
    // Exist restriction to check that PR_SUBJECT exists
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubj);
    pSubjAndRes[0].rt = RES_EXIST;
    pSubjAndRes[0].res.resExist.ulReserved1 = 0;
    pSubjAndRes[0].res.resExist.ulReserved2 = 0;
    pSubjAndRes[0].res.resExist.ulPropTag = PR_SUBJECT;
    // Content restriction to check for "volleyball" in subject
    hResult = MAPIAllocateMore (sizeof(SPropValue), pRest,
            (LPVOID *)&pSubj);
    pSubjAndRes[1].res.resContent.ulFuzzyLevel =
            FL_SUBSTRING | FL_IGNORECASE;
    pSubjAndRes[1].res.resContent.ulPropTag = pSubj->ulPropTag =
            PR_SUBJECT;
    pSubjAndRes[1].res.resContent.lpProp = pSubj;
    pSubj->Value.LPSZ = pszSubjectText;
    return hResult;
}
 
```

## <a name="see-also"></a><span data-ttu-id="c329c-111">Vea también</span><span class="sxs-lookup"><span data-stu-id="c329c-111">See also</span></span>

- [<span data-ttu-id="c329c-112">Tablas MAPI</span><span class="sxs-lookup"><span data-stu-id="c329c-112">MAPI Tables</span></span>](mapi-tables.md)


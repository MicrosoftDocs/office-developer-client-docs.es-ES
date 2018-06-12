---
title: IExchangeModifyTableModifyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.ModifyTable
api_type:
- COM
ms.assetid: b9a745cc-260d-4a1c-896e-6a038ab3cfb9
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 9e7f24fb4b444f63b6277d1844a7948f5ab0c590
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817184"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="585d3-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="585d3-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="585d3-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="585d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="585d3-105">Actualiza un objeto de tabla MAPI.</span><span class="sxs-lookup"><span data-stu-id="585d3-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="585d3-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="585d3-106">Parameters</span></span>

 <span data-ttu-id="585d3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="585d3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="585d3-108">[entrada] Use uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="585d3-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="585d3-109">0 (cero)</span><span class="sxs-lookup"><span data-stu-id="585d3-109">0 (zero)</span></span>
  
> <span data-ttu-id="585d3-110">Use el valor del miembro **ulRowFlags** de la estructura [ROWENTRY](rowentry.md) .</span><span class="sxs-lookup"><span data-stu-id="585d3-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="585d3-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="585d3-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="585d3-112">Establece los derechos de nuevo.</span><span class="sxs-lookup"><span data-stu-id="585d3-112">Sets new rights.</span></span>
    
<span data-ttu-id="585d3-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="585d3-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="585d3-114">Cuando se pasa ACLTABLE_FREEBUSY, proporciona una presentación detallada de derechos de libre/ocupado de nuevo.</span><span class="sxs-lookup"><span data-stu-id="585d3-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="585d3-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="585d3-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="585d3-116">Cuando se pasa ACLTABLE_FREEBUSY, proporciona una presentación sencilla libre/ocupado de derechos de nueva.</span><span class="sxs-lookup"><span data-stu-id="585d3-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="585d3-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="585d3-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="585d3-118">Reemplace todas las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="585d3-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="585d3-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="585d3-119">_lpMods_</span></span>
  
> <span data-ttu-id="585d3-120">[entrada] Apunta a una estructura [ROWLIST](rowlist.md) que contiene las propiedades para el objeto table.</span><span class="sxs-lookup"><span data-stu-id="585d3-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="585d3-121">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="585d3-121">MFCMAPI reference</span></span>

<span data-ttu-id="585d3-122">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="585d3-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="585d3-123">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="585d3-123">**File**</span></span>|<span data-ttu-id="585d3-124">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="585d3-124">**Function**</span></span>|<span data-ttu-id="585d3-125">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="585d3-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="585d3-126">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="585d3-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="585d3-127">CRulesDlg::OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="585d3-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="585d3-128">MFCMAPI usa el método **IExchangeModifyTable::ModifyTable** volver a escribir una regla modificada en la tabla de reglas.</span><span class="sxs-lookup"><span data-stu-id="585d3-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="585d3-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="585d3-129">See also</span></span>



[<span data-ttu-id="585d3-130">IExchangeModifyTable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="585d3-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="585d3-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="585d3-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="585d3-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="585d3-132">ROWLIST</span></span>](rowlist.md)


[<span data-ttu-id="585d3-133">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="585d3-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


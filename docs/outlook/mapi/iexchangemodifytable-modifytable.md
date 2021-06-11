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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 46bb9b2cc1a4d54807d6929b4e1439b58fb3a531
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418179"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="30d7c-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="30d7c-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="30d7c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30d7c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30d7c-105">Actualiza un objeto de tabla MAPI.</span><span class="sxs-lookup"><span data-stu-id="30d7c-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="30d7c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="30d7c-106">Parameters</span></span>

 <span data-ttu-id="30d7c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="30d7c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="30d7c-108">[in] Use uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="30d7c-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="30d7c-109">0 (cero)</span><span class="sxs-lookup"><span data-stu-id="30d7c-109">0 (zero)</span></span>
  
> <span data-ttu-id="30d7c-110">Use el valor del **miembro ulRowFlags** de la [estructura ROWENTRY.](rowentry.md)</span><span class="sxs-lookup"><span data-stu-id="30d7c-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="30d7c-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="30d7c-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="30d7c-112">Establece nuevos derechos.</span><span class="sxs-lookup"><span data-stu-id="30d7c-112">Sets new rights.</span></span>
    
<span data-ttu-id="30d7c-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="30d7c-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="30d7c-114">Cuando ACLTABLE_FREEBUSY se pasa, proporciona una presentación detallada de los nuevos derechos de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="30d7c-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="30d7c-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="30d7c-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="30d7c-116">Cuando ACLTABLE_FREEBUSY se pasa, proporciona una presentación sencilla de los nuevos derechos de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="30d7c-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="30d7c-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="30d7c-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="30d7c-118">Reemplace todas las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="30d7c-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="30d7c-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="30d7c-119">_lpMods_</span></span>
  
> <span data-ttu-id="30d7c-120">[in] Apunta a una [estructura ROWLIST](rowlist.md) que contiene las propiedades del objeto table.</span><span class="sxs-lookup"><span data-stu-id="30d7c-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="30d7c-121">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="30d7c-121">MFCMAPI reference</span></span>

<span data-ttu-id="30d7c-122">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="30d7c-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="30d7c-123">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="30d7c-123">**File**</span></span>|<span data-ttu-id="30d7c-124">**Función**</span><span class="sxs-lookup"><span data-stu-id="30d7c-124">**Function**</span></span>|<span data-ttu-id="30d7c-125">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="30d7c-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="30d7c-126">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="30d7c-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="30d7c-127">CRulesDlg::OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="30d7c-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="30d7c-128">MFCMAPI usa el **método IExchangeModifyTable::ModifyTable** para escribir una regla modificada en la tabla de reglas.</span><span class="sxs-lookup"><span data-stu-id="30d7c-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="30d7c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="30d7c-129">See also</span></span>



[<span data-ttu-id="30d7c-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="30d7c-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="30d7c-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="30d7c-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="30d7c-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="30d7c-132">ROWLIST</span></span>](rowlist.md)


[<span data-ttu-id="30d7c-133">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="30d7c-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


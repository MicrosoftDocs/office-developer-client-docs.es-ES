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
ms.openlocfilehash: b801bdc06317738448a2205b60b94e1c9707d4f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565910"
---
# <a name="iexchangemodifytablemodifytable"></a><span data-ttu-id="02c53-103">IExchangeModifyTable::ModifyTable</span><span class="sxs-lookup"><span data-stu-id="02c53-103">IExchangeModifyTable::ModifyTable</span></span>

  
  
<span data-ttu-id="02c53-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02c53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02c53-105">Actualiza un objeto de tabla MAPI.</span><span class="sxs-lookup"><span data-stu-id="02c53-105">Updates a MAPI table object.</span></span>
  
```cpp
HRESULT ModifyTable( 
  ULONG ulFlags, 
  LPROWLIST lpMods 
); 

```

## <a name="parameters"></a><span data-ttu-id="02c53-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="02c53-106">Parameters</span></span>

 <span data-ttu-id="02c53-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="02c53-107">_ulFlags_</span></span>
  
> <span data-ttu-id="02c53-108">[entrada] Use uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="02c53-108">[in] Use one of the following values:</span></span> 
    
<span data-ttu-id="02c53-109">0 (cero)</span><span class="sxs-lookup"><span data-stu-id="02c53-109">0 (zero)</span></span>
  
> <span data-ttu-id="02c53-110">Use el valor del miembro **ulRowFlags** de la estructura [ROWENTRY](rowentry.md) .</span><span class="sxs-lookup"><span data-stu-id="02c53-110">Use the value of the **ulRowFlags** member of the [ROWENTRY](rowentry.md) structure.</span></span> 
    
<span data-ttu-id="02c53-111">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="02c53-111">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="02c53-112">Establece los derechos de nuevo.</span><span class="sxs-lookup"><span data-stu-id="02c53-112">Sets new rights.</span></span>
    
<span data-ttu-id="02c53-113">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="02c53-113">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="02c53-114">Cuando se pasa ACLTABLE_FREEBUSY, proporciona una presentación detallada de derechos de libre/ocupado de nuevo.</span><span class="sxs-lookup"><span data-stu-id="02c53-114">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="02c53-115">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="02c53-115">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="02c53-116">Cuando se pasa ACLTABLE_FREEBUSY, proporciona una presentación sencilla libre/ocupado de derechos de nueva.</span><span class="sxs-lookup"><span data-stu-id="02c53-116">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
<span data-ttu-id="02c53-117">ROWLIST_REPLACE</span><span class="sxs-lookup"><span data-stu-id="02c53-117">ROWLIST_REPLACE</span></span>
  
> <span data-ttu-id="02c53-118">Reemplace todas las filas de la tabla.</span><span class="sxs-lookup"><span data-stu-id="02c53-118">Replace all the rows in the table.</span></span>
    
 <span data-ttu-id="02c53-119">_lpMods_</span><span class="sxs-lookup"><span data-stu-id="02c53-119">_lpMods_</span></span>
  
> <span data-ttu-id="02c53-120">[entrada] Apunta a una estructura [ROWLIST](rowlist.md) que contiene las propiedades para el objeto table.</span><span class="sxs-lookup"><span data-stu-id="02c53-120">[in] Points to a [ROWLIST](rowlist.md) structure containing the properties for the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="02c53-121">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="02c53-121">MFCMAPI reference</span></span>

<span data-ttu-id="02c53-122">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="02c53-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="02c53-123">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="02c53-123">**File**</span></span>|<span data-ttu-id="02c53-124">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="02c53-124">**Function**</span></span>|<span data-ttu-id="02c53-125">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="02c53-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="02c53-126">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="02c53-126">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="02c53-127">CRulesDlg::OnModifySelectedItem</span><span class="sxs-lookup"><span data-stu-id="02c53-127">CRulesDlg::OnModifySelectedItem</span></span>  <br/> |<span data-ttu-id="02c53-128">MFCMAPI usa el método **IExchangeModifyTable::ModifyTable** volver a escribir una regla modificada en la tabla de reglas.</span><span class="sxs-lookup"><span data-stu-id="02c53-128">MFCMAPI uses the **IExchangeModifyTable::ModifyTable** method to write a modified rule back to the table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="02c53-129">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="02c53-129">See also</span></span>



[<span data-ttu-id="02c53-130">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="02c53-130">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)
  
[<span data-ttu-id="02c53-131">ROWENTRY</span><span class="sxs-lookup"><span data-stu-id="02c53-131">ROWENTRY</span></span>](rowentry.md)
  
[<span data-ttu-id="02c53-132">ROWLIST</span><span class="sxs-lookup"><span data-stu-id="02c53-132">ROWLIST</span></span>](rowlist.md)


[<span data-ttu-id="02c53-133">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="02c53-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


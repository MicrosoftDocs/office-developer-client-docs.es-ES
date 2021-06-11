---
title: IExchangeModifyTableGetTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetTable
api_type:
- COM
ms.assetid: 97df32c4-07c6-41f1-84e7-c6e87d396e34
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 87c60f424e08eea011bb643041196ca9445a3aa1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436247"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="ba52b-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="ba52b-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="ba52b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba52b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba52b-105">Devuelve un puntero a una interfaz para un objeto de tabla MAPI.</span><span class="sxs-lookup"><span data-stu-id="ba52b-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="ba52b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ba52b-106">Parameters</span></span>

 <span data-ttu-id="ba52b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ba52b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ba52b-108">[in] Reservado; debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="ba52b-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="ba52b-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="ba52b-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="ba52b-110">Establece nuevos derechos.</span><span class="sxs-lookup"><span data-stu-id="ba52b-110">Sets new rights.</span></span>
    
<span data-ttu-id="ba52b-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="ba52b-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="ba52b-112">Cuando ACLTABLE_FREEBUSY se pasa, proporciona una presentación detallada de los nuevos derechos de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="ba52b-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="ba52b-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="ba52b-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="ba52b-114">Cuando ACLTABLE_FREEBUSY se pasa, proporciona una presentación sencilla de los nuevos derechos de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="ba52b-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="ba52b-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="ba52b-115">_lppTable_</span></span>
  
> <span data-ttu-id="ba52b-116">[salida] Apunta a una [interfaz IMAPITable : IUnknown](imapitableiunknown.md) que contiene el objeto table.</span><span class="sxs-lookup"><span data-stu-id="ba52b-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="ba52b-117">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ba52b-117">MFCMAPI reference</span></span>

<span data-ttu-id="ba52b-118">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ba52b-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ba52b-119">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ba52b-119">**File**</span></span>|<span data-ttu-id="ba52b-120">**Función**</span><span class="sxs-lookup"><span data-stu-id="ba52b-120">**Function**</span></span>|<span data-ttu-id="ba52b-121">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ba52b-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba52b-122">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ba52b-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="ba52b-123">CRulesDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="ba52b-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="ba52b-124">MFCMAPI usa el **método IExchangeModifyTable::GetTable** para obtener una tabla de reglas.</span><span class="sxs-lookup"><span data-stu-id="ba52b-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba52b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba52b-125">See also</span></span>



[<span data-ttu-id="ba52b-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba52b-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="ba52b-127">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="ba52b-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


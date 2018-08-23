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
ms.openlocfilehash: d28ce67c6b45f3d0b04d645946ea3f4b3a263c48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578993"
---
# <a name="iexchangemodifytablegettable"></a><span data-ttu-id="cbe69-103">IExchangeModifyTable::GetTable</span><span class="sxs-lookup"><span data-stu-id="cbe69-103">IExchangeModifyTable::GetTable</span></span>

  
  
<span data-ttu-id="cbe69-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cbe69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cbe69-105">Devuelve un puntero a una interfaz para un objeto de tabla MAPI.</span><span class="sxs-lookup"><span data-stu-id="cbe69-105">Returns a pointer to an interface for a MAPI table object.</span></span>
  
```cpp
HRESULT GetTable( 
  ULONG ulFlags, 
  LPMAPITABLE FAR * lppTable 
); 

```

## <a name="parameters"></a><span data-ttu-id="cbe69-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="cbe69-106">Parameters</span></span>

 <span data-ttu-id="cbe69-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cbe69-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cbe69-108">[entrada] Reservado; debe ser 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="cbe69-108">[in] Reserved; must be 0 (zero).</span></span>
    
<span data-ttu-id="cbe69-109">ACLTABLE_FREEBUSY</span><span class="sxs-lookup"><span data-stu-id="cbe69-109">ACLTABLE_FREEBUSY</span></span>
  
> <span data-ttu-id="cbe69-110">Establece los derechos de nuevo.</span><span class="sxs-lookup"><span data-stu-id="cbe69-110">Sets new rights.</span></span>
    
<span data-ttu-id="cbe69-111">frightsFreeBusyDetailed</span><span class="sxs-lookup"><span data-stu-id="cbe69-111">frightsFreeBusyDetailed</span></span>
  
> <span data-ttu-id="cbe69-112">Cuando se pasa ACLTABLE_FREEBUSY, proporciona una presentación detallada de derechos de libre/ocupado de nuevo.</span><span class="sxs-lookup"><span data-stu-id="cbe69-112">When ACLTABLE_FREEBUSY is passed, provides a detailed display of new free/busy rights.</span></span>
    
<span data-ttu-id="cbe69-113">frightsFreeBusySimple</span><span class="sxs-lookup"><span data-stu-id="cbe69-113">frightsFreeBusySimple</span></span>
  
> <span data-ttu-id="cbe69-114">Cuando se pasa ACLTABLE_FREEBUSY, proporciona una presentación sencilla libre/ocupado de derechos de nueva.</span><span class="sxs-lookup"><span data-stu-id="cbe69-114">When ACLTABLE_FREEBUSY is passed, provides a simple display of new free/busy rights.</span></span>
    
 <span data-ttu-id="cbe69-115">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="cbe69-115">_lppTable_</span></span>
  
> <span data-ttu-id="cbe69-116">[out] Apunta a un [IMAPITable: IUnknown](imapitableiunknown.md) interfaz que contiene el objeto table.</span><span class="sxs-lookup"><span data-stu-id="cbe69-116">[out] Points to a [IMAPITable : IUnknown](imapitableiunknown.md) interface containing the table object.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="cbe69-117">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cbe69-117">MFCMAPI reference</span></span>

<span data-ttu-id="cbe69-118">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="cbe69-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cbe69-119">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="cbe69-119">**File**</span></span>|<span data-ttu-id="cbe69-120">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="cbe69-120">**Function**</span></span>|<span data-ttu-id="cbe69-121">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="cbe69-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cbe69-122">RulesDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="cbe69-122">RulesDlg.cpp</span></span>  <br/> |<span data-ttu-id="cbe69-123">CRulesDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="cbe69-123">CRulesDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="cbe69-124">MFCMAPI usa el método **IExchangeModifyTable::GetTable** para obtener una tabla de reglas.</span><span class="sxs-lookup"><span data-stu-id="cbe69-124">MFCMAPI uses the **IExchangeModifyTable::GetTable** method to get a table of rules.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cbe69-125">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="cbe69-125">See also</span></span>



[<span data-ttu-id="cbe69-126">IExchangeModifyTable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cbe69-126">IExchangeModifyTable : IUnknown</span></span>](iexchangemodifytableiunknown.md)


[<span data-ttu-id="cbe69-127">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="cbe69-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)


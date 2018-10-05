---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Informes de progreso para enumeración y reajuste de citas.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384356"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="f4f67-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="f4f67-103">RebaseTaskProgress</span></span>

<span data-ttu-id="f4f67-104">Informes de progreso para enumeración y reajuste de citas.</span><span class="sxs-lookup"><span data-stu-id="f4f67-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f4f67-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="f4f67-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f4f67-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f4f67-106">Header file:</span></span>  <br/> |<span data-ttu-id="f4f67-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="f4f67-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="f4f67-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f4f67-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f4f67-109">Aplicaciones cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="f4f67-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="f4f67-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f4f67-110">Called by:</span></span>  <br/> |<span data-ttu-id="f4f67-111">Objeto de reajuste de Outlook</span><span class="sxs-lookup"><span data-stu-id="f4f67-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="f4f67-112">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="f4f67-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="f4f67-113">**PFNREBASETASKPROGRESS** tal como se define en tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="f4f67-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="f4f67-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f4f67-114">Parameters</span></span>

<span data-ttu-id="f4f67-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="f4f67-115">_ulMin_</span></span>
  
> <span data-ttu-id="f4f67-116">[entrada] El extremo inferior del intervalo de citas que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="f4f67-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="f4f67-117">Normalmente, es cero.</span><span class="sxs-lookup"><span data-stu-id="f4f67-117">It is usually zero.</span></span>
    
<span data-ttu-id="f4f67-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="f4f67-118">_ulMax_</span></span>
  
> <span data-ttu-id="f4f67-119">[entrada] Alta final del intervalo de citas que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="f4f67-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="f4f67-120">Suele ser el número de elementos en la carpeta de calendario que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="f4f67-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="f4f67-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="f4f67-121">_ulCur_</span></span>
  
> <span data-ttu-id="f4f67-122">[entrada] El elemento actual que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="f4f67-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="f4f67-123">_State_</span><span class="sxs-lookup"><span data-stu-id="f4f67-123">_State_</span></span>
  
> <span data-ttu-id="f4f67-124">[entrada] Un valor que indica el estado de la que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="f4f67-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="f4f67-125">La enumeración **REBASE_APPT_STATE** se define en tzmovelib.h.</span><span class="sxs-lookup"><span data-stu-id="f4f67-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="f4f67-126">_Estado_ es uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="f4f67-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="f4f67-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** : examen y examen de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4f67-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="f4f67-128">**REBASE_APPT_STATE_SCANNING_FOUND** : examen y que se encuentre un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4f67-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="f4f67-129">**REBASE_APPT_STATE_BEGIN** : fijación e inicio de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4f67-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="f4f67-130">**REBASE_APPT_STATE_REBASING** : fijación y el ajuste de un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4f67-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="f4f67-131">**REBASE_APPT_STATE_SENDING** : fijación y enviar una actualización de la reunión.</span><span class="sxs-lookup"><span data-stu-id="f4f67-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="f4f67-132">**REBASE_APPT_STATE_DONE** : fijación y listo con un elemento.</span><span class="sxs-lookup"><span data-stu-id="f4f67-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="f4f67-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="f4f67-133">_pRowCur_</span></span>
  
> <span data-ttu-id="f4f67-134">[entrada] Un puntero a una estructura **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que describe el elemento que se examinan o fijo.</span><span class="sxs-lookup"><span data-stu-id="f4f67-134">[in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="f4f67-135">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="f4f67-135">Return values</span></span>

<span data-ttu-id="f4f67-136">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="f4f67-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f4f67-137">Notas</span><span class="sxs-lookup"><span data-stu-id="f4f67-137">Remarks</span></span>

<span data-ttu-id="f4f67-138">Las aplicaciones de cliente MAPI que usan la interfaz [IOlkApptRebaser](iolkapptrebaser.md) implementan esta función para realizar un seguimiento de procesamiento del elemento.</span><span class="sxs-lookup"><span data-stu-id="f4f67-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f4f67-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="f4f67-139">See also</span></span>

- [<span data-ttu-id="f4f67-140">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="f4f67-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)


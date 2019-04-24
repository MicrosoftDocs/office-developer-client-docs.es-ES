---
title: RebaseTaskProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8b8368d2-b04b-42a5-fdc3-955fc873c2f5
description: Informa del progreso de la enumeración y el reajuste de las citas.
ms.openlocfilehash: e5df0cd6df10ab86b1a125b9807637438976726f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326456"
---
# <a name="rebasetaskprogress"></a><span data-ttu-id="efb17-103">RebaseTaskProgress</span><span class="sxs-lookup"><span data-stu-id="efb17-103">RebaseTaskProgress</span></span>

<span data-ttu-id="efb17-104">Informa del progreso de la enumeración y el reajuste de las citas.</span><span class="sxs-lookup"><span data-stu-id="efb17-104">Reports progress for enumeration and rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="efb17-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="efb17-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="efb17-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="efb17-106">Header file:</span></span>  <br/> |<span data-ttu-id="efb17-107">tzmovelib. h</span><span class="sxs-lookup"><span data-stu-id="efb17-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="efb17-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="efb17-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="efb17-109">Aplicaciones cliente de MAPI</span><span class="sxs-lookup"><span data-stu-id="efb17-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="efb17-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="efb17-110">Called by:</span></span>  <br/> |<span data-ttu-id="efb17-111">Objeto de reajuste de Outlook</span><span class="sxs-lookup"><span data-stu-id="efb17-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="efb17-112">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="efb17-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="efb17-113">**PFNREBASETASKPROGRESS** como se define en tzmovelib. h</span><span class="sxs-lookup"><span data-stu-id="efb17-113">**PFNREBASETASKPROGRESS** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskProgress(  
    ULONG ulMin, 
    ULONG ulMax, 
    ULONG ulCur, 
    REBASE_APPT_STATE State, 
    const SRow* pRowCur); 

```

## <a name="parameters"></a><span data-ttu-id="efb17-114">Parameters</span><span class="sxs-lookup"><span data-stu-id="efb17-114">Parameters</span></span>

<span data-ttu-id="efb17-115">_ulMin_</span><span class="sxs-lookup"><span data-stu-id="efb17-115">_ulMin_</span></span>
  
> <span data-ttu-id="efb17-116">a El extremo inferior del intervalo de citas que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="efb17-116">[in] The low end of the range of appointments being processed.</span></span> <span data-ttu-id="efb17-117">Suele ser cero.</span><span class="sxs-lookup"><span data-stu-id="efb17-117">It is usually zero.</span></span>
    
<span data-ttu-id="efb17-118">_ulMax_</span><span class="sxs-lookup"><span data-stu-id="efb17-118">_ulMax_</span></span>
  
> <span data-ttu-id="efb17-119">a El extremo superior del intervalo de citas que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="efb17-119">[in] The high end of the range of appointments being processed.</span></span> <span data-ttu-id="efb17-120">Suele ser el número de elementos de la carpeta de calendario que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="efb17-120">It is usually the number of items in the calendar folder being processed.</span></span>
    
<span data-ttu-id="efb17-121">_ulCur_</span><span class="sxs-lookup"><span data-stu-id="efb17-121">_ulCur_</span></span>
  
> <span data-ttu-id="efb17-122">a Elemento actual que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="efb17-122">[in] The current item being processed.</span></span>
    
<span data-ttu-id="efb17-123">_State_</span><span class="sxs-lookup"><span data-stu-id="efb17-123">_State_</span></span>
  
> <span data-ttu-id="efb17-124">a Un valor que indica el estado del elemento que se está procesando.</span><span class="sxs-lookup"><span data-stu-id="efb17-124">[in] A value that indicates the status of the item being processed.</span></span> <span data-ttu-id="efb17-125">La enumeración **REBASE_APPT_STATE** se define en tzmovelib. h.</span><span class="sxs-lookup"><span data-stu-id="efb17-125">The enumeration **REBASE_APPT_STATE** is defined in tzmovelib.h.</span></span>  <span data-ttu-id="efb17-126">_State_ es uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="efb17-126">_State_ is one of the following values:</span></span> 
    
   - <span data-ttu-id="efb17-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** : análisis y examen de un elemento.</span><span class="sxs-lookup"><span data-stu-id="efb17-127">**REBASE_APPT_STATE_SCANNING_EXAMINING** —Scanning and examining an item.</span></span> 
    
   - <span data-ttu-id="efb17-128">**REBASE_APPT_STATE_SCANNING_FOUND** : análisis y encontrado un elemento.</span><span class="sxs-lookup"><span data-stu-id="efb17-128">**REBASE_APPT_STATE_SCANNING_FOUND** —Scanning and found an item.</span></span> 
    
   - <span data-ttu-id="efb17-129">**REBASE_APPT_STATE_BEGIN** : corrección e inicio de un elemento.</span><span class="sxs-lookup"><span data-stu-id="efb17-129">**REBASE_APPT_STATE_BEGIN** —Fixing and starting an item.</span></span> 
    
   - <span data-ttu-id="efb17-130">**REBASE_APPT_STATE_REBASING** : corrección y ajuste de un elemento.</span><span class="sxs-lookup"><span data-stu-id="efb17-130">**REBASE_APPT_STATE_REBASING** —Fixing and adjusting an item.</span></span> 
    
   - <span data-ttu-id="efb17-131">**REBASE_APPT_STATE_SENDING** : corrección y envío de una actualización de la reunión.</span><span class="sxs-lookup"><span data-stu-id="efb17-131">**REBASE_APPT_STATE_SENDING** —Fixing and sending a meeting update.</span></span> 
    
   - <span data-ttu-id="efb17-132">**REBASE_APPT_STATE_DONE** : se corrige y se hace con un elemento.</span><span class="sxs-lookup"><span data-stu-id="efb17-132">**REBASE_APPT_STATE_DONE** —Fixing and done with an item.</span></span> 
    
<span data-ttu-id="efb17-133">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="efb17-133">_pRowCur_</span></span>
  
> <span data-ttu-id="efb17-134">a Un puntero a una estructura **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que describe el elemento que se está examinando o corrigiendo.</span><span class="sxs-lookup"><span data-stu-id="efb17-134">[in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure that describes the item being scanned or fixed.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="efb17-135">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="efb17-135">Return values</span></span>

<span data-ttu-id="efb17-136">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="efb17-136">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="efb17-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="efb17-137">Remarks</span></span>

<span data-ttu-id="efb17-138">Las aplicaciones de cliente MAPI que usan la interfaz [IOlkApptRebaser](iolkapptrebaser.md) implementan esta función para realizar un seguimiento del procesamiento de elementos.</span><span class="sxs-lookup"><span data-stu-id="efb17-138">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track item processing.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="efb17-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="efb17-139">See also</span></span>

- [<span data-ttu-id="efb17-140">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="efb17-140">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)


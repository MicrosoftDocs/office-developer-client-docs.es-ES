---
title: RebaseTaskComplete
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2de5c77c-3fac-cfb6-3719-68df4013cf11
description: Informa de la finalización para el reabado de citas.
ms.openlocfilehash: 9fab0d06bf0b9856b9a968f5c0db1bb15b0fe0bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328325"
---
# <a name="rebasetaskcomplete"></a><span data-ttu-id="00e09-103">RebaseTaskComplete</span><span class="sxs-lookup"><span data-stu-id="00e09-103">RebaseTaskComplete</span></span>

<span data-ttu-id="00e09-104">Informa de la finalización para el reabado de citas.</span><span class="sxs-lookup"><span data-stu-id="00e09-104">Reports completion for rebasing of appointments.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="00e09-105">Información rápida</span><span class="sxs-lookup"><span data-stu-id="00e09-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00e09-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="00e09-106">Header file:</span></span>  <br/> |<span data-ttu-id="00e09-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="00e09-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="00e09-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="00e09-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="00e09-109">Aplicaciones cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="00e09-109">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="00e09-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="00e09-110">Called by:</span></span>  <br/> |<span data-ttu-id="00e09-111">Outlook rebasing (objeto)</span><span class="sxs-lookup"><span data-stu-id="00e09-111">Outlook rebasing object</span></span>  <br/> |
|<span data-ttu-id="00e09-112">Tipo de puntero:</span><span class="sxs-lookup"><span data-stu-id="00e09-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="00e09-113">**PFNREBASETASKCOMPLETE** como se define en tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="00e09-113">**PFNREBASETASKCOMPLETE** as defined in tzmovelib.h</span></span>  <br/> |
   
```cpp
void STDAPICALLTYPE RebaseTaskComplete(  
    ULONG ulRowIndex, 
    const SRow* pRowCur, 
    HRESULT hrResult, 
    BOOL fModified, 
    BOOL fSentUpdate, 
    const MAPIERROR* pError); 

```

## <a name="parameters"></a><span data-ttu-id="00e09-114">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00e09-114">Parameters</span></span>

<span data-ttu-id="00e09-115">_ulRowIndex_</span><span class="sxs-lookup"><span data-stu-id="00e09-115">_ulRowIndex_</span></span>
  
> <span data-ttu-id="00e09-116">[entrada] Fila que se procesó.</span><span class="sxs-lookup"><span data-stu-id="00e09-116">[in] The row that was processed.</span></span> <span data-ttu-id="00e09-117">Este índice hace referencia a la **[estructura SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** pasada a [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span><span class="sxs-lookup"><span data-stu-id="00e09-117">This index refers to the **[SRowSet](https://msdn.microsoft.com/library/7e3761be-afd6-46cb-9a08-25e9016c1241%28Office.15%29.aspx)** structure passed to [IOlkApptRebaser::BeginRebaseAppointments](iolkapptrebaser-beginrebaseappointments.md).</span></span>
    
<span data-ttu-id="00e09-118">_pRowCur_</span><span class="sxs-lookup"><span data-stu-id="00e09-118">_pRowCur_</span></span>
  
> <span data-ttu-id="00e09-119">in] Puntero a una estructura **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** que describe el elemento que se procesó.</span><span class="sxs-lookup"><span data-stu-id="00e09-119">in] A pointer to an **[SRow](https://msdn.microsoft.com/library/369c2d5c-8c2b-4314-9cb2-aaa89580aa2b%28Office.15%29.aspx)** structure describing the item that was processed.</span></span> 
    
<span data-ttu-id="00e09-120">_hrResult_</span><span class="sxs-lookup"><span data-stu-id="00e09-120">_hrResult_</span></span>
  
> <span data-ttu-id="00e09-121">[entrada] HRESULT **que** indica el resultado de la operación de reababamiento.</span><span class="sxs-lookup"><span data-stu-id="00e09-121">[in] An **HRESULT** indicating the result of the rebasing operation.</span></span> 
    
<span data-ttu-id="00e09-122">_fModified_</span><span class="sxs-lookup"><span data-stu-id="00e09-122">_fModified_</span></span>
  
> <span data-ttu-id="00e09-123">[entrada] Especifica si se modificó el elemento.</span><span class="sxs-lookup"><span data-stu-id="00e09-123">[in] Specifies whether the item was modified.</span></span>
    
<span data-ttu-id="00e09-124">_fSentUpdate_</span><span class="sxs-lookup"><span data-stu-id="00e09-124">_fSentUpdate_</span></span>
  
> <span data-ttu-id="00e09-125">[entrada] Especifica si se envió un mensaje de actualización de reunión.</span><span class="sxs-lookup"><span data-stu-id="00e09-125">[in] Specifies whether a meeting update message was sent.</span></span> 
    
<span data-ttu-id="00e09-126">_pError_</span><span class="sxs-lookup"><span data-stu-id="00e09-126">_pError_</span></span>
  
> <span data-ttu-id="00e09-127">[entrada] Puntero a una **estructura MAPIERROR** con información de error extendida.</span><span class="sxs-lookup"><span data-stu-id="00e09-127">[in] A pointer to a **MAPIERROR** structure with extended error information.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="00e09-128">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="00e09-128">Return values</span></span>

<span data-ttu-id="00e09-129">S_OK si la llamada se realiza correctamente; de lo contrario, un código de error.</span><span class="sxs-lookup"><span data-stu-id="00e09-129">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00e09-130">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00e09-130">Remarks</span></span>

<span data-ttu-id="00e09-131">Las aplicaciones cliente MAPI que usan [la interfaz IOlkApptRebaser](iolkapptrebaser.md) implementan esta función para realizar un seguimiento de la finalización de las actualizaciones de elementos.</span><span class="sxs-lookup"><span data-stu-id="00e09-131">MAPI client applications that use the [IOlkApptRebaser](iolkapptrebaser.md) interface implement this function to track completion of item updates.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00e09-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="00e09-132">See also</span></span>

- [<span data-ttu-id="00e09-133">Acerca de reajuste mediante programación los calendarios del horario de verano</span><span class="sxs-lookup"><span data-stu-id="00e09-133">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)


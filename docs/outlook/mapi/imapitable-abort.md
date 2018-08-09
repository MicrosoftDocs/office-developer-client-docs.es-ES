---
title: IMAPITableAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Abort
api_type:
- COM
ms.assetid: 73291a5b-b626-494c-b5d9-f7709e34bac2
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4b578f287a532475b53fb69cc4499662b6c4b6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817574"
---
# <a name="imapitableabort"></a><span data-ttu-id="92813-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="92813-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="92813-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="92813-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="92813-105">Detiene cualquier operación asincrónica actualmente en curso para la tabla.</span><span class="sxs-lookup"><span data-stu-id="92813-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="92813-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92813-106">Parameters</span></span>

<span data-ttu-id="92813-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="92813-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="92813-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92813-108">Return value</span></span>

<span data-ttu-id="92813-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="92813-109">S_OK</span></span> 
  
> <span data-ttu-id="92813-110">Uno o más de las operaciones asincrónicas se han detenido.</span><span class="sxs-lookup"><span data-stu-id="92813-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="92813-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="92813-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="92813-112">Una operación asincrónica está en curso y no se puede detener o ya se ha completado.</span><span class="sxs-lookup"><span data-stu-id="92813-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="92813-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="92813-113">Remarks</span></span>

<span data-ttu-id="92813-114">El método **IMAPITable::Abort** detiene cualquier operación asincrónica que está actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="92813-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="92813-115">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="92813-115">Notes to callers</span></span>

<span data-ttu-id="92813-116">Para averiguar si una operación asincrónica está en curso, llame al método [IMAPITable::GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="92813-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="92813-117">Si los **botones Anular** , se detiene el procesamiento de una llamada al método [IMAPITable:: Restrict](imapitable-restrict.md) , el estado de la tabla será tal como estaba en el momento en que se procesa la llamada **Anular** .</span><span class="sxs-lookup"><span data-stu-id="92813-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="92813-118">Si los **botones Anular** , se detiene el procesamiento de una llamada al método [SortTable](imapitable-sorttable.md) , criterio de ordenación de la tabla no se ve afectado y permanece tal como estaba antes de la llamada **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="92813-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92813-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="92813-119">See also</span></span>



[<span data-ttu-id="92813-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="92813-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="92813-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="92813-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="92813-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="92813-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="92813-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="92813-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


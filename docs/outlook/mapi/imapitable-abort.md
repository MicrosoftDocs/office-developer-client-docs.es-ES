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
ms.openlocfilehash: 68d40a6e152698554fcb88c6f7e5bfd4a7ff0ce3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574009"
---
# <a name="imapitableabort"></a><span data-ttu-id="11ce0-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="11ce0-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="11ce0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11ce0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11ce0-105">Detiene cualquier operación asincrónica actualmente en curso para la tabla.</span><span class="sxs-lookup"><span data-stu-id="11ce0-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="11ce0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11ce0-106">Parameters</span></span>

<span data-ttu-id="11ce0-107">Ninguna</span><span class="sxs-lookup"><span data-stu-id="11ce0-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="11ce0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11ce0-108">Return value</span></span>

<span data-ttu-id="11ce0-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="11ce0-109">S_OK</span></span> 
  
> <span data-ttu-id="11ce0-110">Uno o más de las operaciones asincrónicas se han detenido.</span><span class="sxs-lookup"><span data-stu-id="11ce0-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="11ce0-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="11ce0-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="11ce0-112">Una operación asincrónica está en curso y no se puede detener o ya se ha completado.</span><span class="sxs-lookup"><span data-stu-id="11ce0-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="11ce0-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11ce0-113">Remarks</span></span>

<span data-ttu-id="11ce0-114">El método **IMAPITable::Abort** detiene cualquier operación asincrónica que está actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="11ce0-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="11ce0-115">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="11ce0-115">Notes to callers</span></span>

<span data-ttu-id="11ce0-116">Para averiguar si una operación asincrónica está en curso, llame al método [IMAPITable::GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="11ce0-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="11ce0-117">Si los **botones Anular** , se detiene el procesamiento de una llamada al método [IMAPITable:: Restrict](imapitable-restrict.md) , el estado de la tabla será tal como estaba en el momento en que se procesa la llamada **Anular** .</span><span class="sxs-lookup"><span data-stu-id="11ce0-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="11ce0-118">Si los **botones Anular** , se detiene el procesamiento de una llamada al método [SortTable](imapitable-sorttable.md) , criterio de ordenación de la tabla no se ve afectado y permanece tal como estaba antes de la llamada **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="11ce0-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="11ce0-119">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="11ce0-119">See also</span></span>



[<span data-ttu-id="11ce0-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="11ce0-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="11ce0-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="11ce0-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="11ce0-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="11ce0-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="11ce0-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11ce0-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


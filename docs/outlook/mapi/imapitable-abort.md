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
ms.openlocfilehash: 74c307fca27f1adec18d236792f8a58d97e33ec5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406153"
---
# <a name="imapitableabort"></a><span data-ttu-id="950a4-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="950a4-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="950a4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="950a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="950a4-105">Detiene las operaciones asincrónicas actualmente en curso para la tabla.</span><span class="sxs-lookup"><span data-stu-id="950a4-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="950a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="950a4-106">Parameters</span></span>

<span data-ttu-id="950a4-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="950a4-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="950a4-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="950a4-108">Return value</span></span>

<span data-ttu-id="950a4-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="950a4-109">S_OK</span></span> 
  
> <span data-ttu-id="950a4-110">Se han detenido una o varias operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="950a4-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="950a4-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="950a4-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="950a4-112">Una operación asincrónica está en curso y no se puede detener o ya se ha completado.</span><span class="sxs-lookup"><span data-stu-id="950a4-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="950a4-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="950a4-113">Remarks</span></span>

<span data-ttu-id="950a4-114">El **método IMAPITable::Abort** detiene cualquier operación asincrónica que esté en curso.</span><span class="sxs-lookup"><span data-stu-id="950a4-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="950a4-115">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="950a4-115">Notes to callers</span></span>

<span data-ttu-id="950a4-116">Para averiguar si hay una operación asincrónica en curso, llame al [método IMAPITable::GetStatus.](imapitable-getstatus.md)</span><span class="sxs-lookup"><span data-stu-id="950a4-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="950a4-117">Si **Abort** detiene el procesamiento de una llamada al método [IMAPITable::Restrict,](imapitable-restrict.md) el estado de  la tabla será el mismo que en el momento en que se procese la llamada de anulación.</span><span class="sxs-lookup"><span data-stu-id="950a4-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="950a4-118">Si **Abort** detiene el procesamiento de una llamada al método [IMAPITable::SortTable,](imapitable-sorttable.md) el criterio de ordenación de la tabla no se verán afectados y permanecerá igual que antes de la llamada **a SortTable.**</span><span class="sxs-lookup"><span data-stu-id="950a4-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="950a4-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="950a4-119">See also</span></span>



[<span data-ttu-id="950a4-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="950a4-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="950a4-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="950a4-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="950a4-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="950a4-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="950a4-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="950a4-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328960"
---
# <a name="imapitableabort"></a><span data-ttu-id="cd212-103">IMAPITable::Abort</span><span class="sxs-lookup"><span data-stu-id="cd212-103">IMAPITable::Abort</span></span>

  
  
<span data-ttu-id="cd212-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd212-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd212-105">Detiene todas las operaciones asincrónicas que se encuentran en curso para la tabla.</span><span class="sxs-lookup"><span data-stu-id="cd212-105">Stops any asynchronous operations currently in progress for the table.</span></span>
  
```cpp
HRESULT Abort( void );
```

## <a name="parameters"></a><span data-ttu-id="cd212-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd212-106">Parameters</span></span>

<span data-ttu-id="cd212-107">Ninguno</span><span class="sxs-lookup"><span data-stu-id="cd212-107">None</span></span>
  
## <a name="return-value"></a><span data-ttu-id="cd212-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd212-108">Return value</span></span>

<span data-ttu-id="cd212-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="cd212-109">S_OK</span></span> 
  
> <span data-ttu-id="cd212-110">Se han detenido una o más operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="cd212-110">One or more asynchronous operations have been stopped.</span></span>
    
<span data-ttu-id="cd212-111">MAPI_E_UNABLE_TO_ABORT</span><span class="sxs-lookup"><span data-stu-id="cd212-111">MAPI_E_UNABLE_TO_ABORT</span></span> 
  
> <span data-ttu-id="cd212-112">Una operación asincrónica está en curso y no se puede detener o ya se ha completado.</span><span class="sxs-lookup"><span data-stu-id="cd212-112">An asynchronous operation is in progress and cannot be stopped or it has already completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cd212-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd212-113">Remarks</span></span>

<span data-ttu-id="cd212-114">El método **IMAPITable:: ABORT** detiene cualquier operación asincrónica que esté actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="cd212-114">The **IMAPITable::Abort** method stops any asynchronous operation that is currently in progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="cd212-115">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="cd212-115">Notes to callers</span></span>

<span data-ttu-id="cd212-116">Para averiguar si una operación asincrónica está en curso, llame al método [IMAPITable:: getStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="cd212-116">To find out if an asynchronous operation is in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
<span data-ttu-id="cd212-117">Si **Abort** detiene el procesamiento de una llamada al método [IMAPITable:: Restrict](imapitable-restrict.md) , el estado de la tabla será el que se encontraba en el momento en que se procesa la llamada a **Abort** .</span><span class="sxs-lookup"><span data-stu-id="cd212-117">If **Abort** halts the processing of a call to the [IMAPITable::Restrict](imapitable-restrict.md) method, the state of the table will be as it was at the time the **Abort** call is processed.</span></span> 
  
<span data-ttu-id="cd212-118">Si **Abort** detiene el procesamiento de una llamada al método [IMAPITable:: SortTable](imapitable-sorttable.md) , el criterio de ordenación de la tabla no se ve afectado y permanece como era antes de la llamada a **SortTable** .</span><span class="sxs-lookup"><span data-stu-id="cd212-118">If **Abort** halts the processing of a call to the [IMAPITable::SortTable](imapitable-sorttable.md) method, the table's sort order is unaffected and remains as it was before the **SortTable** call.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd212-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd212-119">See also</span></span>



[<span data-ttu-id="cd212-120">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="cd212-120">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="cd212-121">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="cd212-121">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="cd212-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="cd212-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="cd212-123">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd212-123">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


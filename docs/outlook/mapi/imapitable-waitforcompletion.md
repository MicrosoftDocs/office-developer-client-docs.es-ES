---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407063"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="8f303-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="8f303-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="8f303-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8f303-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8f303-105">Suspende el procesamiento hasta que se hayan completado una o varias operaciones asincrónicas en curso en la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f303-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="8f303-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8f303-106">Parameters</span></span>

 <span data-ttu-id="8f303-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8f303-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8f303-108">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8f303-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8f303-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="8f303-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="8f303-110">[entrada] Número máximo de milisegundos que hay que esperar a que se complete la operación asincrónica o las operaciones.</span><span class="sxs-lookup"><span data-stu-id="8f303-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="8f303-111">Para esperar indefinidamente hasta que se produzca la finalización,  _establezca ulTimeout_ en 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="8f303-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="8f303-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="8f303-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="8f303-113">[entrada, salida] En la entrada, un puntero válido o NULL.</span><span class="sxs-lookup"><span data-stu-id="8f303-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="8f303-114">En el resultado,  _si lpulTableStatus es_ un puntero válido, apunta al estado más reciente de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f303-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="8f303-115">Si  _lpulTableStatus es_ NULL, no se devuelve información de estado.</span><span class="sxs-lookup"><span data-stu-id="8f303-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="8f303-116">Si **WaitForCompletion devuelve** un valor HRESULT fallido, el contenido de  _lpulTableStatus_ no está definido.</span><span class="sxs-lookup"><span data-stu-id="8f303-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8f303-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8f303-117">Return value</span></span>

<span data-ttu-id="8f303-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8f303-118">S_OK</span></span> 
  
> <span data-ttu-id="8f303-119">La operación de espera se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8f303-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="8f303-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8f303-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8f303-121">La tabla no admite esperar a que se completen las operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="8f303-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="8f303-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="8f303-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="8f303-123">La operación asincrónica o las operaciones no se completaron en la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="8f303-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8f303-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8f303-124">Remarks</span></span>

<span data-ttu-id="8f303-125">El **método IMAPITable::WaitForCompletion** suspende el procesamiento hasta que se completen las operaciones asincrónicas actualmente en curso para la tabla.</span><span class="sxs-lookup"><span data-stu-id="8f303-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="8f303-126">**WaitForCompletion** puede permitir que las operaciones asincrónicas se completen completamente o se ejecuten durante un determinado número de milisegundos, como se indica en  _ulTimeout_, antes de ser interrumpidas.</span><span class="sxs-lookup"><span data-stu-id="8f303-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="8f303-127">Para detectar operaciones asincrónicas en curso, llame al [método IMAPITable::GetStatus.](imapitable-getstatus.md)</span><span class="sxs-lookup"><span data-stu-id="8f303-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f303-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8f303-128">See also</span></span>



[<span data-ttu-id="8f303-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="8f303-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="8f303-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="8f303-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="8f303-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="8f303-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="8f303-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="8f303-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="8f303-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="8f303-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="8f303-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f303-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


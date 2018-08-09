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
ms.openlocfilehash: c7859e033924786e415f9faa9f75021ea47968c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817608"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="8a41f-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="8a41f-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="8a41f-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8a41f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8a41f-105">Suspende el procesamiento hasta que han completado una o varias operaciones asincrónicas en curso en la tabla.</span><span class="sxs-lookup"><span data-stu-id="8a41f-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="8a41f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="8a41f-106">Parameters</span></span>

 <span data-ttu-id="8a41f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8a41f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8a41f-108">Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8a41f-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="8a41f-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="8a41f-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="8a41f-110">[entrada] Número máximo de milisegundos de espera para que las operaciones para llevar a cabo o la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="8a41f-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="8a41f-111">Para esperar indefinidamente hasta que se produce la finalización, establezca _ulTimeout_ en 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="8a41f-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="8a41f-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="8a41f-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="8a41f-113">[entrada, salida] En la entrada, un puntero válido o un valor NULL.</span><span class="sxs-lookup"><span data-stu-id="8a41f-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="8a41f-114">En la salida, si _lpulTableStatus_ es un puntero válido, apunta al estado más reciente de la tabla.</span><span class="sxs-lookup"><span data-stu-id="8a41f-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="8a41f-115">Si _lpulTableStatus_ es NULL, no se devuelve ninguna información de estado.</span><span class="sxs-lookup"><span data-stu-id="8a41f-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="8a41f-116">Si **WaitForCompletion** devuelve un valor HRESULT realizado correctamente, el contenido de _lpulTableStatus_ es indefinido.</span><span class="sxs-lookup"><span data-stu-id="8a41f-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8a41f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8a41f-117">Return value</span></span>

<span data-ttu-id="8a41f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8a41f-118">S_OK</span></span> 
  
> <span data-ttu-id="8a41f-119">La operación de espera fue correcta.</span><span class="sxs-lookup"><span data-stu-id="8a41f-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="8a41f-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8a41f-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8a41f-121">La tabla no es compatible con la espera para la finalización de las operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="8a41f-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="8a41f-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="8a41f-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="8a41f-123">Las operaciones o una operación asincrónica no se completó en el tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="8a41f-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8a41f-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8a41f-124">Remarks</span></span>

<span data-ttu-id="8a41f-125">El método **IMAPITable::WaitForCompletion** suspende el procesamiento hasta que han completado las operaciones asincrónicas actualmente en curso para la tabla.</span><span class="sxs-lookup"><span data-stu-id="8a41f-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="8a41f-126">**WaitForCompletion** puede permitir que las operaciones asincrónicas a totalmente completa o para que se ejecute durante un determinado número de milisegundos, como se indica en _ulTimeout_, antes de que se interrumpa.</span><span class="sxs-lookup"><span data-stu-id="8a41f-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="8a41f-127">Para detectar las operaciones asincrónicas en curso, llame al método [IMAPITable::GetStatus](imapitable-getstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="8a41f-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8a41f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a41f-128">See also</span></span>



[<span data-ttu-id="8a41f-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="8a41f-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="8a41f-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="8a41f-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="8a41f-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="8a41f-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="8a41f-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="8a41f-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="8a41f-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="8a41f-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="8a41f-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8a41f-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


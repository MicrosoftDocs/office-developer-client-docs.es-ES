---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ab92aee6a8254a16c48352e371b711932bbe7427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817390"
---
# <a name="imapiprogressgetmin"></a><span data-ttu-id="97c61-103">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="97c61-103">IMAPIProgress::GetMin</span></span>

  
  
<span data-ttu-id="97c61-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="97c61-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="97c61-105">Devuelve el valor mínimo en el método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) de progreso que se muestra la información.</span><span class="sxs-lookup"><span data-stu-id="97c61-105">Returns the minimum value in the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span> 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a><span data-ttu-id="97c61-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97c61-106">Parameters</span></span>

 <span data-ttu-id="97c61-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="97c61-107">_lpulMin_</span></span>
  
> <span data-ttu-id="97c61-108">[out] Un puntero al número mínimo de elementos de la operación.</span><span class="sxs-lookup"><span data-stu-id="97c61-108">[out] A pointer to the minimum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="97c61-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97c61-109">Return value</span></span>

<span data-ttu-id="97c61-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="97c61-110">S_OK</span></span> 
  
> <span data-ttu-id="97c61-111">Se ha recuperado el número mínimo de elementos de la operación.</span><span class="sxs-lookup"><span data-stu-id="97c61-111">The minimum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97c61-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97c61-112">Remarks</span></span>

<span data-ttu-id="97c61-113">El valor mínimo representa el inicio de la operación con formato numérico.</span><span class="sxs-lookup"><span data-stu-id="97c61-113">The minimum value represents the start of the operation in numeric form.</span></span> <span data-ttu-id="97c61-114">El valor puede ser un valor máximo global, usado para representar el ámbito de la pantalla de progreso todo, o un valor local, que se usa para representar sólo una parte de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="97c61-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="97c61-115">El valor de la opción marca determina si el objeto de progreso comprende el valor mínimo para ser local o global.</span><span class="sxs-lookup"><span data-stu-id="97c61-115">The value of the flag setting affects whether the progress object understands the minimum value to be local or global.</span></span> <span data-ttu-id="97c61-116">Cuando se establece la marca MAPI_TOP_LEVEL, el valor mínimo se considera que es global y se utiliza para calcular el progreso de toda la operación.</span><span class="sxs-lookup"><span data-stu-id="97c61-116">When the MAPI_TOP_LEVEL flag is set, the minimum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="97c61-117">Cuando MAPI_TOP_LEVEL no está establecido, el valor mínimo se considera local y proveedores de utilizan internamente para mostrar el progreso de subobjetos de nivel inferiores.</span><span class="sxs-lookup"><span data-stu-id="97c61-117">When MAPI_TOP_LEVEL is not set, the minimum value is considered local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="97c61-118">Objetos de progreso guardar el valor mínimo local sólo para devolver a un proveedor a través de una llamada **GetMin** .</span><span class="sxs-lookup"><span data-stu-id="97c61-118">Progress objects save the local minimum value only to return it to a provider through a **GetMin** call.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="97c61-119">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="97c61-119">Notes to implementers</span></span>

<span data-ttu-id="97c61-120">Inicializar el valor mínimo en 1.</span><span class="sxs-lookup"><span data-stu-id="97c61-120">Initialize the minimum value to 1.</span></span> <span data-ttu-id="97c61-121">Proveedores de servicios pueden restablecer este valor llamando al método **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="97c61-121">Service providers can reset this value by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="97c61-122">Para obtener más información acerca de cómo implementar otros métodos [IMAPIProgress](imapiprogressiunknown.md) y **GetMin** , vea [implementar un indicador de progreso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="97c61-122">For more information about how to implement **GetMin** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="97c61-123">Para que obtener más información acerca de cómo y cuándo se deben realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="97c61-123">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="97c61-124">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="97c61-124">MFCMAPI reference</span></span>

<span data-ttu-id="97c61-125">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="97c61-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="97c61-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="97c61-126">**File**</span></span>|<span data-ttu-id="97c61-127">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="97c61-127">**Function**</span></span>|<span data-ttu-id="97c61-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="97c61-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="97c61-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="97c61-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="97c61-130">CMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="97c61-130">CMAPIProgress::GetMin</span></span>  <br/> |<span data-ttu-id="97c61-131">MFCMAPI usa el método **IMAPIProgress::GetMin** para obtener el valor mínimo para el indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="97c61-131">MFCMAPI uses the **IMAPIProgress::GetMin** method to get the minimum value for the progress indicator.</span></span> <span data-ttu-id="97c61-132">Devuelve el valor 1 a menos que se hayan establecido previamente límites llamando al método **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="97c61-132">Returns 1 unless limits have been previously set by calling the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="97c61-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="97c61-133">See also</span></span>



[<span data-ttu-id="97c61-134">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="97c61-134">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="97c61-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="97c61-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="97c61-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="97c61-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="97c61-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="97c61-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="97c61-138">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="97c61-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="97c61-139">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="97c61-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="97c61-140">Implementar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="97c61-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


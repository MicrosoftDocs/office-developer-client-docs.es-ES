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
ms.openlocfilehash: 6cd31f8ac713c21053db7ef461220a360ebeec74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331685"
---
# <a name="imapiprogressgetmin"></a><span data-ttu-id="13e56-103">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="13e56-103">IMAPIProgress::GetMin</span></span>

  
  
<span data-ttu-id="13e56-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="13e56-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="13e56-105">Devuelve el valor mínimo del método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) para el que se muestra información de progreso.</span><span class="sxs-lookup"><span data-stu-id="13e56-105">Returns the minimum value in the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method for which progress information is displayed.</span></span> 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a><span data-ttu-id="13e56-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13e56-106">Parameters</span></span>

 <span data-ttu-id="13e56-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="13e56-107">_lpulMin_</span></span>
  
> <span data-ttu-id="13e56-108">[salida] Un puntero al número mínimo de elementos de la operación.</span><span class="sxs-lookup"><span data-stu-id="13e56-108">[out] A pointer to the minimum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="13e56-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13e56-109">Return value</span></span>

<span data-ttu-id="13e56-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="13e56-110">S_OK</span></span> 
  
> <span data-ttu-id="13e56-111">El número mínimo de elementos de la operación que se ha recuperado.</span><span class="sxs-lookup"><span data-stu-id="13e56-111">The minimum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="13e56-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="13e56-112">Remarks</span></span>

<span data-ttu-id="13e56-113">El valor mínimo representa el inicio de la operación en formato numérico.</span><span class="sxs-lookup"><span data-stu-id="13e56-113">The minimum value represents the start of the operation in numeric form.</span></span> <span data-ttu-id="13e56-114">El valor puede ser un valor máximo global, usado para representar el ámbito de la pantalla de progreso total, o un valor local, para representar únicamente una parte de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="13e56-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="13e56-115">El valor de la configuración de la etiqueta determina si el objeto de progreso comprende el valor mínimo local o global.</span><span class="sxs-lookup"><span data-stu-id="13e56-115">The value of the flag setting affects whether the progress object understands the minimum value to be local or global.</span></span> <span data-ttu-id="13e56-116">Cuando se establece la etiqueta MAPI_TOP_LEVEL, el valor mínimo se considera global y se usa para calcular el progreso de toda la operación.</span><span class="sxs-lookup"><span data-stu-id="13e56-116">When the MAPI_TOP_LEVEL flag is set, the minimum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="13e56-117">Cuando no se establece MAPI_TOP_LEVEL, el valor mínimo se considera local y los proveedores lo usan internamente para mostrar el progreso de objetos secundarios de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="13e56-117">When MAPI_TOP_LEVEL is not set, the minimum value is considered local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="13e56-118">Los objetos de progreso guardan el valor mínimo local solo para devolverlo a un proveedor a través de una llamada **GetMin**.</span><span class="sxs-lookup"><span data-stu-id="13e56-118">Progress objects save the local minimum value only to return it to a provider through a **GetMin** call.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="13e56-119">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="13e56-119">Notes to implementers</span></span>

<span data-ttu-id="13e56-120">Inicialice el valor mínimo en 1.</span><span class="sxs-lookup"><span data-stu-id="13e56-120">Initialize the minimum value to 1.</span></span> <span data-ttu-id="13e56-121">Los proveedores de servicios pueden restablecer este valor llamando al método **IMAPIProgress::SetLimits**.</span><span class="sxs-lookup"><span data-stu-id="13e56-121">Service providers can reset this value by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="13e56-122">Para obtener más información sobre cómo implementar **GetMin** y otros métodos [IMAPIProgress](imapiprogressiunknown.md), vea [Implementar un indicador de progreso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="13e56-122">For more information about how to implement **GetMin** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="13e56-123">Para obtener más información sobre cómo y cuándo debe realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="13e56-123">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="13e56-124">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="13e56-124">MFCMAPI reference</span></span>

<span data-ttu-id="13e56-125">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="13e56-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="13e56-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="13e56-126">**File**</span></span>|<span data-ttu-id="13e56-127">**Función**</span><span class="sxs-lookup"><span data-stu-id="13e56-127">**Function**</span></span>|<span data-ttu-id="13e56-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="13e56-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="13e56-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="13e56-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="13e56-130">CMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="13e56-130">CMAPIProgress::GetMin</span></span>  <br/> |<span data-ttu-id="13e56-131">MFCMAPI usa el método **IMAPIProgress::GetMin** para obtener el valor mínimo para el indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="13e56-131">MFCMAPI uses the **IMAPIProgress::GetMin** method to get the minimum value for the progress indicator.</span></span> <span data-ttu-id="13e56-132">Devuelve el valor 1 a menos que se hayan establecido límites anteriormente llamando al método **IMAPIProgress::SetLimits**.</span><span class="sxs-lookup"><span data-stu-id="13e56-132">Returns 1 unless limits have been previously set by calling the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13e56-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="13e56-133">See also</span></span>



[<span data-ttu-id="13e56-134">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="13e56-134">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="13e56-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="13e56-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="13e56-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="13e56-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="13e56-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="13e56-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="13e56-138">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="13e56-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="13e56-139">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="13e56-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="13e56-140">Implementar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="13e56-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


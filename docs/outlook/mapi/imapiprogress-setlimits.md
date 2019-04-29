---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421469"
---
# <a name="imapiprogresssetlimits"></a><span data-ttu-id="4b6e0-103">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="4b6e0-103">IMAPIProgress::SetLimits</span></span>

  
  
<span data-ttu-id="4b6e0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b6e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4b6e0-105">Establece los límites inferior y superior para el número de elementos de la operación y las marcas que controlan cómo se calcula la información de progreso de la operación.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-105">Sets the lower and upper limits for the number of items in the operation, and the flags that control how progress information is calculated for the operation.</span></span>
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4b6e0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4b6e0-106">Parameters</span></span>

 <span data-ttu-id="4b6e0-107">_lpulMin_</span><span class="sxs-lookup"><span data-stu-id="4b6e0-107">_lpulMin_</span></span>
  
> <span data-ttu-id="4b6e0-108">a Un puntero a una variable que contiene el límite inferior de los elementos de la operación.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-108">[in] A pointer to a variable that contains the lower limit of items in the operation.</span></span>
    
 <span data-ttu-id="4b6e0-109">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="4b6e0-109">_lpulMax_</span></span>
  
> <span data-ttu-id="4b6e0-110">a Un puntero a una variable que contiene el límite superior de los elementos de la operación.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-110">[in] A pointer to a variable that contains the upper limit of items in the operation.</span></span>
    
 <span data-ttu-id="4b6e0-111">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="4b6e0-111">_lpulFlags_</span></span>
  
> <span data-ttu-id="4b6e0-112">a Máscara de máscara de marcadores que controla el nivel de funcionamiento en el que se calcula la información del progreso.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-112">[in] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="4b6e0-113">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="4b6e0-113">The following flag can be set:</span></span>
    
<span data-ttu-id="4b6e0-114">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="4b6e0-114">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="4b6e0-115">Utiliza los valores de los parámetros _ulCount_ y _UlTotal_ del método [método imapiprogress::P rogress](imapiprogress-progress.md) , que indican el elemento actualmente procesado y los elementos totales, respectivamente, para incrementar el progreso de la operación.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-115">Uses the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters, which indicate the currently processed item and the total items, respectively, to increment progress on the operation.</span></span> <span data-ttu-id="4b6e0-116">Cuando se establece este indicador, se deben establecer los valores de los límites inferior y superior globales.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-116">When this flag is set, the values of the global lower and upper limits have to be set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4b6e0-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4b6e0-117">Return value</span></span>

<span data-ttu-id="4b6e0-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4b6e0-118">S_OK</span></span> 
  
> <span data-ttu-id="4b6e0-119">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4b6e0-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4b6e0-120">Remarks</span></span>

<span data-ttu-id="4b6e0-121">Los proveedores de servicios llaman al método **método imapiprogress:: SetLimits** para establecer o borrar la marca MAPI_TOP_LEVEL y para establecer valores mínimos y máximos locales y globales.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-121">Service providers call the **IMAPIProgress::SetLimits** method to set or clear the MAPI_TOP_LEVEL flag and to set local and global minimum and maximum values.</span></span> <span data-ttu-id="4b6e0-122">El valor de la configuración de la marca determina si el objeto Progress comprende los valores mínimos y máximos locales o globales.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-122">The value of the flag setting affects whether the progress object understands the minimum and maximum values to be local or global.</span></span> <span data-ttu-id="4b6e0-123">Cuando se establece la marca MAPI_TOP_LEVEL, estos valores se consideran globales y se usan para calcular el progreso de toda la operación.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-123">When the MAPI_TOP_LEVEL flag is set, these values are considered global and are used to calculate progress for the entire operation.</span></span> <span data-ttu-id="4b6e0-124">Los objetos de progreso inicializan el valor mínimo global en 1 y el valor máximo global en 1000.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-124">Progress objects initialize the global minimum value to 1 and the global maximum value to 1000.</span></span> 
  
<span data-ttu-id="4b6e0-125">Cuando MAPI_TOP_LEVEL no se establece, los valores mínimos y máximos se consideran locales y los proveedores los usan internamente para mostrar el progreso de los subobjetos de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-125">When MAPI_TOP_LEVEL is not set, the minimum and maximum values are considered local, and providers use them internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="4b6e0-126">Los objetos de progreso guardan los valores mínimos y máximos locales solo para que se puedan devolver a los proveedores cuando se llama a los métodos [método imapiprogress:: GetMin](imapiprogress-getmin.md) y [método imapiprogress:: GetMax](imapiprogress-getmax.md) .</span><span class="sxs-lookup"><span data-stu-id="4b6e0-126">Progress objects save the local minimum and maximum values only so that they can be returned to providers when the [IMAPIProgress::GetMin](imapiprogress-getmin.md) and [IMAPIProgress::GetMax](imapiprogress-getmax.md) methods are called.</span></span> 
  
<span data-ttu-id="4b6e0-127">Para obtener más información sobre cómo implementar **SetLimits** y los otros métodos de [método imapiprogress](imapiprogressiunknown.md) , consulte [implementación de un indicador de progreso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="4b6e0-127">For more information about how to implement **SetLimits** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
<span data-ttu-id="4b6e0-128">Para obtener más información sobre cómo y cuándo debe realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="4b6e0-128">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4b6e0-129">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4b6e0-129">MFCMAPI reference</span></span>

<span data-ttu-id="4b6e0-130">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-130">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4b6e0-131">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="4b6e0-131">**File**</span></span>|<span data-ttu-id="4b6e0-132">**Función**</span><span class="sxs-lookup"><span data-stu-id="4b6e0-132">**Function**</span></span>|<span data-ttu-id="4b6e0-133">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="4b6e0-133">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4b6e0-134">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="4b6e0-134">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="4b6e0-135">CMAPIProgress:: SetLimits</span><span class="sxs-lookup"><span data-stu-id="4b6e0-135">CMAPIProgress::SetLimits</span></span>  <br/> |<span data-ttu-id="4b6e0-136">MFCMAPI usa el método **método imapiprogress:: SetLimits** para establecer los límites máximos y mínimos y los marcadores del objeto Progress.</span><span class="sxs-lookup"><span data-stu-id="4b6e0-136">MFCMAPI uses the **IMAPIProgress::SetLimits** method to set the maximum and minimum limits and flags for the progress object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4b6e0-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="4b6e0-137">See also</span></span>



[<span data-ttu-id="4b6e0-138">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="4b6e0-138">IMAPIProgress::GetMax</span></span>](imapiprogress-getmax.md)
  
[<span data-ttu-id="4b6e0-139">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="4b6e0-139">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="4b6e0-140">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="4b6e0-140">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="4b6e0-141">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4b6e0-141">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="4b6e0-142">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="4b6e0-142">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="4b6e0-143">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="4b6e0-143">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="4b6e0-144">Implementar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="4b6e0-144">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


---
title: IMAPIProgressGetFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9a5e4205a808c7a6e469d2e9cb0a1b3c17a92d21
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573547"
---
# <a name="imapiprogressgetflags"></a><span data-ttu-id="f37ca-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="f37ca-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="f37ca-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f37ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f37ca-105">Devuelve marca configuración desde el objeto de progreso para el nivel de operación en la que se calcula la información de progreso.</span><span class="sxs-lookup"><span data-stu-id="f37ca-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f37ca-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f37ca-106">Parameters</span></span>

 <span data-ttu-id="f37ca-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="f37ca-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="f37ca-108">[out] Una máscara de bits de indicadores que controla el nivel de operación en progreso que se calcula de la información.</span><span class="sxs-lookup"><span data-stu-id="f37ca-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="f37ca-109">Se puede devolver la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="f37ca-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="f37ca-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="f37ca-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="f37ca-111">Progreso se que se calcula para el objeto de nivel superior, el objeto que se llama por el cliente a comenzar la operación.</span><span class="sxs-lookup"><span data-stu-id="f37ca-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="f37ca-112">Por ejemplo, el objeto de nivel superior en una operación de copia de la carpeta es la carpeta que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="f37ca-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="f37ca-113">Cuando no se establece MAPI_TOP_LEVEL, progreso se calcula para un objeto de nivel inferior o subobjetos.</span><span class="sxs-lookup"><span data-stu-id="f37ca-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="f37ca-114">En la operación de copia de la carpeta, un objeto de nivel inferior es una de las subcarpetas en la carpeta que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="f37ca-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f37ca-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f37ca-115">Return value</span></span>

<span data-ttu-id="f37ca-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f37ca-116">S_OK</span></span> 
  
> <span data-ttu-id="f37ca-117">El valor de flags se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="f37ca-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f37ca-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f37ca-118">Remarks</span></span>

<span data-ttu-id="f37ca-119">MAPI permite a los proveedores de servicio diferenciar entre objetos de nivel superior y subobjetos con el indicador MAPI_TOP_LEVEL para que todos los objetos implicados en una operación pueden usar la misma implementación de [IMAPIProgress](imapiprogressiunknown.md) para mostrar el progreso.</span><span class="sxs-lookup"><span data-stu-id="f37ca-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="f37ca-120">Esto hace que la visualización del indicador se realice correctamente en un solo sentido positivo.</span><span class="sxs-lookup"><span data-stu-id="f37ca-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="f37ca-121">Si se establece la marca MAPI_TOP_LEVEL determina cómo los proveedores de servicios establecen los demás parámetros en llamadas posteriores al objeto de progreso.</span><span class="sxs-lookup"><span data-stu-id="f37ca-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="f37ca-122">El valor devuelto por **GetFlags** se establece inicialmente el implementador y posteriormente por el proveedor de servicios a través de una llamada al método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) .</span><span class="sxs-lookup"><span data-stu-id="f37ca-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f37ca-123">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="f37ca-123">Notes to implementers</span></span>

<span data-ttu-id="f37ca-124">Inicializar siempre la marca a MAPI_TOP_LEVEL y, a continuación, se basan en proveedores de servicios para desactivarla cuando sea apropiado.</span><span class="sxs-lookup"><span data-stu-id="f37ca-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="f37ca-125">Proveedores de servicios pueden borrar y restablecer el indicador llamando al método **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="f37ca-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="f37ca-126">Para obtener más información acerca de cómo implementar **GetFlags** y los otros métodos de **IMAPIProgress** , vea [implementar un indicador de progreso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="f37ca-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="f37ca-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="f37ca-127">Notes to callers</span></span>

<span data-ttu-id="f37ca-128">Cuando se muestra un indicador de progreso, realizar su primera llamada a una llamada a **IMAPIProgress::GetFlags**.</span><span class="sxs-lookup"><span data-stu-id="f37ca-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="f37ca-129">El valor devuelto debe ser MAPI_TOP_LEVEL, debido a que todas las implementaciones de inicialización el contenido del parámetro _lpulFlags_ para este valor.</span><span class="sxs-lookup"><span data-stu-id="f37ca-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="f37ca-130">Para obtener más información acerca de la secuencia de llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="f37ca-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f37ca-131">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f37ca-131">MFCMAPI reference</span></span>

<span data-ttu-id="f37ca-132">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="f37ca-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f37ca-133">**File**</span><span class="sxs-lookup"><span data-stu-id="f37ca-133">**File**</span></span>|<span data-ttu-id="f37ca-134">**Función**</span><span class="sxs-lookup"><span data-stu-id="f37ca-134">**Function**</span></span>|<span data-ttu-id="f37ca-135">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="f37ca-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f37ca-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="f37ca-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="f37ca-137">CMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="f37ca-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="f37ca-138">MFCMAPI usa el método **IMAPIProgress::GetFlags** para determinar qué marcas se establecen.</span><span class="sxs-lookup"><span data-stu-id="f37ca-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="f37ca-139">Devuelve MAPI_TOP_LEVEL a menos que se han configurado indicadores mediante el método **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="f37ca-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f37ca-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="f37ca-140">See also</span></span>



[<span data-ttu-id="f37ca-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="f37ca-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="f37ca-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f37ca-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="f37ca-143">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="f37ca-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f37ca-144">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="f37ca-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="f37ca-145">Implementar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="f37ca-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


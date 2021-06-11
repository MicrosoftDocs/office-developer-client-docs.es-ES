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
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423646"
---
# <a name="imapiprogressgetflags"></a><span data-ttu-id="4f32c-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="4f32c-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="4f32c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f32c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f32c-105">Devuelve la configuración de marca del objeto de progreso para el nivel de operación en el que se calcula la información de progreso.</span><span class="sxs-lookup"><span data-stu-id="4f32c-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4f32c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="4f32c-106">Parameters</span></span>

 <span data-ttu-id="4f32c-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="4f32c-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="4f32c-108">[salida] Máscara de bits de marcas que controla el nivel de operación en el que se calcula la información de progreso.</span><span class="sxs-lookup"><span data-stu-id="4f32c-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="4f32c-109">Se puede devolver la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="4f32c-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="4f32c-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="4f32c-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="4f32c-111">El progreso se calcula para el objeto de nivel superior, el objeto al que llama el cliente para iniciar la operación.</span><span class="sxs-lookup"><span data-stu-id="4f32c-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="4f32c-112">Por ejemplo, el objeto de nivel superior de una operación de copia de carpeta es la carpeta que se está copiando.</span><span class="sxs-lookup"><span data-stu-id="4f32c-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="4f32c-113">Cuando MAPI_TOP_LEVEL no se establece, el progreso se calcula para un objeto de nivel inferior o subobjeto.</span><span class="sxs-lookup"><span data-stu-id="4f32c-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="4f32c-114">En la operación de copia de carpeta, un objeto de nivel inferior es una de las subcarpetas de la carpeta que se está copiando.</span><span class="sxs-lookup"><span data-stu-id="4f32c-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4f32c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4f32c-115">Return value</span></span>

<span data-ttu-id="4f32c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f32c-116">S_OK</span></span> 
  
> <span data-ttu-id="4f32c-117">El valor de las marcas se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="4f32c-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f32c-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4f32c-118">Remarks</span></span>

<span data-ttu-id="4f32c-119">MAPI permite a los proveedores de servicios diferenciar entre objetos de nivel superior y subobjetos con la marca MAPI_TOP_LEVEL para que todos los objetos implicados en una operación puedan usar la misma implementación [imapiprogress](imapiprogressiunknown.md) para mostrar el progreso.</span><span class="sxs-lookup"><span data-stu-id="4f32c-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="4f32c-120">Esto hace que la presentación del indicador continúe sin problemas en una sola dirección positiva.</span><span class="sxs-lookup"><span data-stu-id="4f32c-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="4f32c-121">Si se MAPI_TOP_LEVEL marca de acceso determina cómo los proveedores de servicios establecen los demás parámetros en llamadas posteriores al objeto de progreso.</span><span class="sxs-lookup"><span data-stu-id="4f32c-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="4f32c-122">El valor devuelto por **GetFlags** lo establece inicialmente el implementador y posteriormente el proveedor de servicios mediante una llamada al método [IMAPIProgress::SetLimits.](imapiprogress-setlimits.md)</span><span class="sxs-lookup"><span data-stu-id="4f32c-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4f32c-123">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="4f32c-123">Notes to implementers</span></span>

<span data-ttu-id="4f32c-124">Inicialice siempre la marca para MAPI_TOP_LEVEL y, a continuación, confíe en los proveedores de servicios para borrarla cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="4f32c-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="4f32c-125">Los proveedores de servicios pueden borrar y restablecer la marca llamando al método **IMAPIProgress::SetLimits.**</span><span class="sxs-lookup"><span data-stu-id="4f32c-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="4f32c-126">Para obtener más información acerca de cómo implementar **GetFlags** y los demás métodos **IMAPIProgress,** vea [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="4f32c-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4f32c-127">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="4f32c-127">Notes to callers</span></span>

<span data-ttu-id="4f32c-128">Cuando muestre un indicador de progreso, realice la primera llamada a **IMAPIProgress::GetFlags**.</span><span class="sxs-lookup"><span data-stu-id="4f32c-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="4f32c-129">El valor devuelto debe MAPI_TOP_LEVEL, ya que todas las implementaciones inicializan el contenido del parámetro  _lpulFlags_ en este valor.</span><span class="sxs-lookup"><span data-stu-id="4f32c-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="4f32c-130">Para obtener más información acerca de la secuencia de llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="4f32c-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4f32c-131">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4f32c-131">MFCMAPI reference</span></span>

<span data-ttu-id="4f32c-132">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="4f32c-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4f32c-133">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="4f32c-133">**File**</span></span>|<span data-ttu-id="4f32c-134">**Función**</span><span class="sxs-lookup"><span data-stu-id="4f32c-134">**Function**</span></span>|<span data-ttu-id="4f32c-135">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="4f32c-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4f32c-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="4f32c-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="4f32c-137">CMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="4f32c-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="4f32c-138">MFCMAPI usa el **método IMAPIProgress::GetFlags** para determinar qué marcas se establecen.</span><span class="sxs-lookup"><span data-stu-id="4f32c-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="4f32c-139">Devuelve MAPI_TOP_LEVEL a menos que se hayan establecido marcas mediante el método **IMAPIProgress::SetLimits.**</span><span class="sxs-lookup"><span data-stu-id="4f32c-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4f32c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f32c-140">See also</span></span>



[<span data-ttu-id="4f32c-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="4f32c-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="4f32c-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f32c-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="4f32c-143">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="4f32c-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="4f32c-144">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="4f32c-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="4f32c-145">Implementar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="4f32c-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


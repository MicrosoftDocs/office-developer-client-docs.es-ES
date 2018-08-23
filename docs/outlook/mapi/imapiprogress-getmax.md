---
title: IMAPIProgressGetMax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 2dadad410b9aaf1401d792de373e561c29183a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567240"
---
# <a name="imapiprogressgetmax"></a><span data-ttu-id="7a822-103">IMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="7a822-103">IMAPIProgress::GetMax</span></span>

  
  
<span data-ttu-id="7a822-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a822-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a822-105">Devuelve el número máximo de elementos en la operación de progreso que se muestra la información.</span><span class="sxs-lookup"><span data-stu-id="7a822-105">Returns the maximum number of items in the operation for which progress information is displayed.</span></span>
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a><span data-ttu-id="7a822-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a822-106">Parameters</span></span>

 <span data-ttu-id="7a822-107">_lpulMax_</span><span class="sxs-lookup"><span data-stu-id="7a822-107">_lpulMax_</span></span>
  
> <span data-ttu-id="7a822-108">[out] Un puntero al número máximo de elementos de la operación.</span><span class="sxs-lookup"><span data-stu-id="7a822-108">[out] A pointer to the maximum number of items in the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7a822-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a822-109">Return value</span></span>

<span data-ttu-id="7a822-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a822-110">S_OK</span></span> 
  
> <span data-ttu-id="7a822-111">Se ha recuperado el número máximo de elementos de la operación.</span><span class="sxs-lookup"><span data-stu-id="7a822-111">The maximum number of items in the operation has been retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a822-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7a822-112">Remarks</span></span>

<span data-ttu-id="7a822-113">El valor máximo representa el final de la operación con formato numérico.</span><span class="sxs-lookup"><span data-stu-id="7a822-113">The maximum value represents the end of the operation in numeric form.</span></span> <span data-ttu-id="7a822-114">El valor puede ser un valor máximo global, usado para representar el ámbito de la pantalla de progreso todo, o un valor local, que se usa para representar sólo una parte de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="7a822-114">The value can be a global maximum value, used to represent the scope of the entire progress display, or a local value, used to represent only a part of the display.</span></span> 
  
<span data-ttu-id="7a822-115">El valor de la opción marca determina si el objeto de progreso comprende el valor máximo para ser local o global.</span><span class="sxs-lookup"><span data-stu-id="7a822-115">The value of the flag setting affects whether the progress object understands the maximum value to be local or global.</span></span> <span data-ttu-id="7a822-116">Cuando se establece la marca MAPI_TOP_LEVEL, el valor máximo se considera que es global y se utiliza para calcular el progreso de toda la operación.</span><span class="sxs-lookup"><span data-stu-id="7a822-116">When the MAPI_TOP_LEVEL flag is set, the maximum value is considered to be global and is used to calculate progress for the entire operation.</span></span> <span data-ttu-id="7a822-117">Cuando MAPI_TOP_LEVEL no está establecida, se considera que el valor máximo es local, y proveedores de usarlo internamente para mostrar progreso para subobjetos de nivel inferiores.</span><span class="sxs-lookup"><span data-stu-id="7a822-117">When MAPI_TOP_LEVEL is not set, the maximum value is considered to be local, and providers use it internally to display progress for lower level subobjects.</span></span> <span data-ttu-id="7a822-118">Objetos de progreso guardar el valor máximo local sólo para devolver a un proveedor a través de una llamada **GetMax** .</span><span class="sxs-lookup"><span data-stu-id="7a822-118">Progress objects save the local maximum value only to return it to a provider through a **GetMax** call.</span></span> 
  
<span data-ttu-id="7a822-119">Para que obtener más información acerca de cómo y cuándo se deben realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="7a822-119">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7a822-120">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="7a822-120">Notes to implementers</span></span>

<span data-ttu-id="7a822-121">Inicializar el valor máximo en 1000.</span><span class="sxs-lookup"><span data-stu-id="7a822-121">Initialize the maximum value to 1000.</span></span> <span data-ttu-id="7a822-122">Proveedores de servicios pueden restablecer este valor llamando al método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) .</span><span class="sxs-lookup"><span data-stu-id="7a822-122">Service providers can reset this value by calling the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> <span data-ttu-id="7a822-123">Para obtener más información acerca de cómo implementar otros métodos [IMAPIProgress](imapiprogressiunknown.md) y **GetMax** , vea [implementar un indicador de progreso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="7a822-123">For more information about how to implement **GetMax** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7a822-124">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="7a822-124">MFCMAPI reference</span></span>

<span data-ttu-id="7a822-125">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="7a822-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7a822-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="7a822-126">**File**</span></span>|<span data-ttu-id="7a822-127">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="7a822-127">**Function**</span></span>|<span data-ttu-id="7a822-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="7a822-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7a822-129">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="7a822-129">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="7a822-130">CMAPIProgress::GetMax</span><span class="sxs-lookup"><span data-stu-id="7a822-130">CMAPIProgress::GetMax</span></span>  <br/> |<span data-ttu-id="7a822-131">MFCMAPI usa el método **IMAPIProgress::GetMax** para obtener el valor máximo para el objeto de progreso.</span><span class="sxs-lookup"><span data-stu-id="7a822-131">MFCMAPI uses the **IMAPIProgress::GetMax** method to get the maximum value for the progress object.</span></span> <span data-ttu-id="7a822-132">Devuelve 1000 a menos que los límites se han establecido previamente con el método **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="7a822-132">Returns 1000 unless limits have previously been set with the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7a822-133">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="7a822-133">See also</span></span>



[<span data-ttu-id="7a822-134">IMAPIProgress::GetMin</span><span class="sxs-lookup"><span data-stu-id="7a822-134">IMAPIProgress::GetMin</span></span>](imapiprogress-getmin.md)
  
[<span data-ttu-id="7a822-135">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="7a822-135">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="7a822-136">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="7a822-136">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="7a822-137">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a822-137">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="7a822-138">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="7a822-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="7a822-139">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="7a822-139">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="7a822-140">Implementar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="7a822-140">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


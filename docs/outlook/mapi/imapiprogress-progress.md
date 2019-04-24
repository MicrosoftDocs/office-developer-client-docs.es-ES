---
title: IMAPIProgressProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270304"
---
# <a name="imapiprogressprogress"></a><span data-ttu-id="ac4f8-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="ac4f8-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="ac4f8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac4f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac4f8-105">Actualiza el indicador de progreso con una presentación del progreso a medida que se realiza para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="ac4f8-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ac4f8-106">Parameters</span></span>

 <span data-ttu-id="ac4f8-107">_ulValue_</span><span class="sxs-lookup"><span data-stu-id="ac4f8-107">_ulValue_</span></span>
  
> <span data-ttu-id="ac4f8-108">a Número que indica el nivel de progreso actual (calculado a partir de los parámetros _ulCount_ y _ulTotal_ o de los parámetros _LpulMin_ y _lpulMax_ del método [método imapiprogress:: SetLimits](imapiprogress-setlimits.md) ) entre el global límite inferior y el límite superior global.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="ac4f8-109">_ulCount_</span><span class="sxs-lookup"><span data-stu-id="ac4f8-109">_ulCount_</span></span>
  
> <span data-ttu-id="ac4f8-110">a Número que indica el elemento actualmente procesado en relación con el total.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="ac4f8-111">_ulTotal_</span><span class="sxs-lookup"><span data-stu-id="ac4f8-111">_ulTotal_</span></span>
  
> <span data-ttu-id="ac4f8-112">a Número total de elementos que se van a procesar durante la operación.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac4f8-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac4f8-113">Return value</span></span>

<span data-ttu-id="ac4f8-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac4f8-114">S_OK</span></span> 
  
> <span data-ttu-id="ac4f8-115">El indicador de progreso se actualizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="ac4f8-116">Notas a los implementadores</span><span class="sxs-lookup"><span data-stu-id="ac4f8-116">Notes to implementers</span></span>

<span data-ttu-id="ac4f8-117">El parámetro _ulValue_ será igual al valor mínimo global solo al inicio de la operación y al valor máximo global solo al finalizar la operación.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="ac4f8-118">Use los parámetros _ulCount_ y _ulTotal_ , si están disponibles, para mostrar un mensaje opcional como "5 elementos completados de 10".</span><span class="sxs-lookup"><span data-stu-id="ac4f8-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="ac4f8-119">Si _ulCount_ y _ulTotal_ se establecen en 0, decida si desea cambiar visualmente el indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="ac4f8-120">Algunos proveedores de servicios establecen estos parámetros en 0 para indicar que están procesando un subobjeto cuyo progreso se supervisa en relación con un objeto primario.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="ac4f8-121">En esta situación, tiene sentido cambiar la presentación solo cuando el objeto primario informa del progreso.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="ac4f8-122">Algunos proveedores de servicios pasan 0 para estos parámetros cada vez.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="ac4f8-123">Para obtener más información acerca de cómo implementar el **progreso** y los otros métodos [método imapiprogress](imapiprogressiunknown.md) , consulte [implementación de un indicador de progreso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="ac4f8-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ac4f8-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="ac4f8-124">Notes to callers</span></span>

<span data-ttu-id="ac4f8-125">No se necesitan los tres parámetros para **método imapiprogress::P rogress** .</span><span class="sxs-lookup"><span data-stu-id="ac4f8-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="ac4f8-126">El único parámetro necesario es _ulValue_, un número que indica el porcentaje de progreso.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="ac4f8-127">Si se establece la marca MAPI_TOP_LEVEL, también puede pasar un recuento de objetos y un total de objetos.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="ac4f8-128">Algunas implementaciones usan estos valores para mostrar una frase como "5 elementos completados de 10" con el indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="ac4f8-129">Si va a copiar todos los mensajes en una sola carpeta, establezca _ulTotal_ en el número total de mensajes que se copian.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="ac4f8-130">Si va a copiar una carpeta, establezca _ulTotal_ en el número de subcarpetas de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="ac4f8-131">Si la carpeta que se va a copiar no contiene subcarpetas y sólo mensajes, establezca _ulTotal_ en 1.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="ac4f8-132">Para obtener más información sobre cómo y cuándo debe realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="ac4f8-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ac4f8-133">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ac4f8-133">MFCMAPI reference</span></span>

<span data-ttu-id="ac4f8-134">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ac4f8-135">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ac4f8-135">**File**</span></span>|<span data-ttu-id="ac4f8-136">**Función**</span><span class="sxs-lookup"><span data-stu-id="ac4f8-136">**Function**</span></span>|<span data-ttu-id="ac4f8-137">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="ac4f8-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac4f8-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="ac4f8-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="ac4f8-139">CMAPIProgress::P rogress</span><span class="sxs-lookup"><span data-stu-id="ac4f8-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="ac4f8-140">MFCMAPI usa el método **método imapiprogress::P rogress** para actualizar la barra de estado de MFCMAPI con el porcentaje de progreso actual, calculado a partir de _uValue_ y los valores máximos y mínimos actuales.</span><span class="sxs-lookup"><span data-stu-id="ac4f8-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac4f8-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac4f8-141">See also</span></span>



[<span data-ttu-id="ac4f8-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="ac4f8-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="ac4f8-143">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac4f8-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="ac4f8-144">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="ac4f8-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="ac4f8-145">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="ac4f8-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="ac4f8-146">Implementar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="ac4f8-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


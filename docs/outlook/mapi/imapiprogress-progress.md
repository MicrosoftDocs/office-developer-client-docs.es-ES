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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 2a003be35fc9c3ef8efc7c66997ee99f6e578f09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817394"
---
# <a name="imapiprogressprogress"></a><span data-ttu-id="6e4d1-103">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="6e4d1-103">IMAPIProgress::Progress</span></span>

  
  
<span data-ttu-id="6e4d1-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e4d1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e4d1-105">Actualiza el indicador de progreso con una visualización del progreso de la medida que se realiza hacia la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-105">Updates the progress indicator with a display of the progress as it is made toward completion of the operation.</span></span> 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a><span data-ttu-id="6e4d1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e4d1-106">Parameters</span></span>

 <span data-ttu-id="6e4d1-107">_ulValue_</span><span class="sxs-lookup"><span data-stu-id="6e4d1-107">_ulValue_</span></span>
  
> <span data-ttu-id="6e4d1-108">[entrada] Un número que indica el nivel actual de progreso (calculado a partir de los parámetros _ulCount_ y _ulTotal_ o de los parámetros _lpulMin_ y _lpulMax_ del método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) ) entre la información global límite inferior y el límite superior global.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-108">[in] A number that indicates the current level of progress (calculated from the  _ulCount_ and  _ulTotal_ parameters or from the  _lpulMin_ and  _lpulMax_ parameters of the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method) between the global lower limit and the global upper limit.</span></span> 
    
 <span data-ttu-id="6e4d1-109">_ulCount_</span><span class="sxs-lookup"><span data-stu-id="6e4d1-109">_ulCount_</span></span>
  
> <span data-ttu-id="6e4d1-110">[entrada] Un número que indica el elemento procesado actualmente en relación con el total.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-110">[in] A number that indicates the currently processed item relative to the total.</span></span>
    
 <span data-ttu-id="6e4d1-111">_ulTotal_</span><span class="sxs-lookup"><span data-stu-id="6e4d1-111">_ulTotal_</span></span>
  
> <span data-ttu-id="6e4d1-112">[entrada] El número total de elementos que se procesan durante la operación.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-112">[in] The total number of items to be processed during the operation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6e4d1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e4d1-113">Return value</span></span>

<span data-ttu-id="6e4d1-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e4d1-114">S_OK</span></span> 
  
> <span data-ttu-id="6e4d1-115">El indicador de progreso se actualizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-115">The progress indicator was successfully updated.</span></span>
    
## <a name="notes-to-implementers"></a><span data-ttu-id="6e4d1-116">Notas para los implementadores</span><span class="sxs-lookup"><span data-stu-id="6e4d1-116">Notes to implementers</span></span>

<span data-ttu-id="6e4d1-117">El parámetro _ulValue_ será igual al valor mínimo global sólo al principio de la operación y para el valor máximo global sólo en la finalización de la operación.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-117">The  _ulValue_ parameter will be equal to the global minimum value only at the start of the operation and to the global maximum value only at the completion of the operation.</span></span> 
  
<span data-ttu-id="6e4d1-118">Use los parámetros _ulCount_ y _ulTotal_ , si está disponible, para mostrar un mensaje opcional, como "5 elementos completadas del 10".</span><span class="sxs-lookup"><span data-stu-id="6e4d1-118">Use the  _ulCount_ and  _ulTotal_ parameters, if available, to display an optional message such as "5 items completed out of 10."</span></span> <span data-ttu-id="6e4d1-119">Si _ulCount_ y _ulTotal_ se establecen en 0, decida si desea cambiar visualmente el indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-119">If  _ulCount_ and  _ulTotal_ are set to 0, decide whether to visually change the progress indicator.</span></span> <span data-ttu-id="6e4d1-120">Algunos proveedores de servicios establecen estos parámetros en 0 para indicar que va a procesar un subobjetos cuyo progreso se supervisa con respecto a un objeto primario.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-120">Some service providers set these parameters to 0 to indicate that they are processing a subobject whose progress is monitored relative to a parent object.</span></span> <span data-ttu-id="6e4d1-121">En esta situación, tiene sentido para cambiar la presentación sólo cuando el objeto primario informes de progreso.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-121">In this situation, it makes sense to change the display only when the parent object reports progress.</span></span> <span data-ttu-id="6e4d1-122">Algunos proveedores de servicios pasan 0 para estos parámetros cada vez.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-122">Some service providers pass 0 for these parameters every time.</span></span> 
  
<span data-ttu-id="6e4d1-123">Para obtener más información acerca de cómo implementar el **progreso** y los otros métodos de [IMAPIProgress](imapiprogressiunknown.md) , vea [implementar un indicador de progreso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="6e4d1-123">For more information about how to implement **Progress** and the other [IMAPIProgress](imapiprogressiunknown.md) methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="6e4d1-124">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="6e4d1-124">Notes to callers</span></span>

<span data-ttu-id="6e4d1-125">No todos los tres de los parámetros para **IMAPIProgress::Progress** son necesarios.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-125">Not all three of the parameters to **IMAPIProgress::Progress** are required.</span></span> <span data-ttu-id="6e4d1-126">El único parámetro necesario es _ulValue_, un número que indica el porcentaje de progreso.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-126">The only parameter that is required is  _ulValue_, a number that indicates the percentage of progress.</span></span> <span data-ttu-id="6e4d1-127">Si se establece la marca MAPI_TOP_LEVEL, también se pueden pasar un recuento de objetos y un total de objeto.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-127">If the MAPI_TOP_LEVEL flag is set, you can also pass an object count and an object total.</span></span> <span data-ttu-id="6e4d1-128">Algunas implementaciones de utilizan estos valores para mostrar una frase, como "5 elementos completadas del 10" con el indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-128">Some implementations use these values to display a phrase such as "5 items completed out of 10" with the progress indicator.</span></span> 
  
<span data-ttu-id="6e4d1-129">Si va a copiar todos los mensajes en una sola carpeta, establezca _ulTotal_ en el número total de mensajes que se está copiando.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-129">If you are copying all messages in a single folder, set  _ulTotal_ to the total number of messages being copied.</span></span> <span data-ttu-id="6e4d1-130">Si va a copiar una carpeta, establezca _ulTotal_ en el número de subcarpetas de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-130">If you are copying a folder, set  _ulTotal_ to the number of subfolders in the folder.</span></span> <span data-ttu-id="6e4d1-131">Si la carpeta que se va a copiar no contiene subcarpetas y sólo los mensajes, establezca _ulTotal_ en 1.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-131">If the folder to be copied contains no subfolders and only messages, set  _ulTotal_ to 1.</span></span> 
  
<span data-ttu-id="6e4d1-132">Para que obtener más información acerca de cómo y cuándo se deben realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="6e4d1-132">For more information about how and when to make calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6e4d1-133">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6e4d1-133">MFCMAPI reference</span></span>

<span data-ttu-id="6e4d1-134">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-134">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6e4d1-135">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="6e4d1-135">**File**</span></span>|<span data-ttu-id="6e4d1-136">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="6e4d1-136">**Function**</span></span>|<span data-ttu-id="6e4d1-137">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="6e4d1-137">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6e4d1-138">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="6e4d1-138">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="6e4d1-139">CMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="6e4d1-139">CMAPIProgress::Progress</span></span>  <br/> |<span data-ttu-id="6e4d1-140">MFCMAPI usa el método **IMAPIProgress::Progress** para actualizar la barra de estado MFCMAPI con el porcentaje actual de progreso, que se calcula a partir de _uValue_ y los valores máximo y mínimos actuales.</span><span class="sxs-lookup"><span data-stu-id="6e4d1-140">MFCMAPI uses the **IMAPIProgress::Progress** method to update the MFCMAPI status bar with the current percentage of progress, calculated from  _uValue_ and the current maximum and minimum values.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6e4d1-141">Ver también</span><span class="sxs-lookup"><span data-stu-id="6e4d1-141">See also</span></span>



[<span data-ttu-id="6e4d1-142">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="6e4d1-142">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="6e4d1-143">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6e4d1-143">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="6e4d1-144">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="6e4d1-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="6e4d1-145">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="6e4d1-145">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="6e4d1-146">Implementación de un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="6e4d1-146">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)


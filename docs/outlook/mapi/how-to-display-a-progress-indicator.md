---
title: Mostrar un indicador de progreso
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 3c4c553a000dab233eb208c1222cc427c97b1e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816982"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="695f7-103">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="695f7-103">Display a progress indicator</span></span>
 
<span data-ttu-id="695f7-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="695f7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="695f7-105">Para mostrar un indicador de progreso, llame a [IMAPIProgress::GetFlags](imapiprogress-getflags.md) para recuperar los indicadores actuales de configuración.</span><span class="sxs-lookup"><span data-stu-id="695f7-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="695f7-106">Si se establece la marca MAPI_TOP_LEVEL, complete los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="695f7-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="695f7-107">Establezca a una variable igual al número total de elementos que se procesan en la operación.</span><span class="sxs-lookup"><span data-stu-id="695f7-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="695f7-108">Por ejemplo, si va a copiar el contenido de una carpeta, este valor será igual que el número de las subcarpetas de la carpeta más el número de mensajes.</span><span class="sxs-lookup"><span data-stu-id="695f7-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="695f7-109">Establezca a una variable igual a 1000 dividido por el número de elementos.</span><span class="sxs-lookup"><span data-stu-id="695f7-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="695f7-110">Si se muestra el progreso de subobjetos, llamar al método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) del objeto de progreso y pasar los siguientes valores para los tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="695f7-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="695f7-111">Establezca el parámetro _lpulMin_ en 0.</span><span class="sxs-lookup"><span data-stu-id="695f7-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="695f7-112">Establezca el parámetro _lpulMax_ en 1000.</span><span class="sxs-lookup"><span data-stu-id="695f7-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="695f7-113">Establezca el parámetro _lpulFlags_ en MAPI_TOP_LEVEL.</span><span class="sxs-lookup"><span data-stu-id="695f7-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="695f7-114">Para que cada objeto que va a procesar, complete los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="695f7-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="695f7-115">Llame a **IMAPIProgress::SetLimits** y pase los siguientes valores para los tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="695f7-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="695f7-116">Establezca el parámetro _lpulMin_ en la variable establecida en el paso 2 multiplicado por el elemento actual menos 1.</span><span class="sxs-lookup"><span data-stu-id="695f7-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="695f7-117">Establezca el parámetro _lpulMax_ en la variable establecida en el paso 2 multiplicado por el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="695f7-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="695f7-118">Establezca el parámetro _lpulFlags_ en 0.</span><span class="sxs-lookup"><span data-stu-id="695f7-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="695f7-119">Lleve a cabo el procesamiento se debe realizar en este objeto.</span><span class="sxs-lookup"><span data-stu-id="695f7-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="695f7-120">Si se trata de un subobjetos y desea mostrar el progreso en subobjetos, pase un puntero al objeto de progreso en el parámetro _lpProgress_ para el método.</span><span class="sxs-lookup"><span data-stu-id="695f7-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="695f7-121">Llame a [IMAPIProgress::Progress](imapiprogress-progress.md) y pase los siguientes valores para los tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="695f7-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="695f7-122">Establezca el parámetro _ulValue_ en la variable establecida en el paso 2 multiplicado por el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="695f7-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="695f7-123">Establezca el parámetro _ulCount_ en el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="695f7-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="695f7-124">Establezca el parámetro _ulTotal_ en la variable establecida en el paso 1, el número total de objetos.</span><span class="sxs-lookup"><span data-stu-id="695f7-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="695f7-125">Si no está establecido el indicador MAPI_TOP_LEVEL, complete los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="695f7-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="695f7-126">Llamar al método [IMAPIProgress::GetMin](imapiprogress-getmin.md) del objeto de progreso para recuperar el valor mínimo para la presentación.</span><span class="sxs-lookup"><span data-stu-id="695f7-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="695f7-127">Llame a [IMAPIProgress::GetMax](imapiprogress-getmax.md) para recuperar el valor máximo para la presentación.</span><span class="sxs-lookup"><span data-stu-id="695f7-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="695f7-128">Establezca a una variable igual al número total de objetos que va a procesar.</span><span class="sxs-lookup"><span data-stu-id="695f7-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="695f7-129">Establezca a una variable igual al resultado de restar el valor mínimo del valor máximo y, a continuación, dividiendo el número total de objetos.</span><span class="sxs-lookup"><span data-stu-id="695f7-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="695f7-130">Para que cada objeto que va a procesar, complete los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="695f7-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="695f7-131">Si su proveedor es que muestra el progreso de subobjetos, llamar **IMAPIProgress::SetLimits** y pasar los siguientes valores para los tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="695f7-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="695f7-132">Establezca el parámetro _lpulMin_ en el valor mínimo más el elemento actual menos 1 multiplicado por la variable establecida en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="695f7-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="695f7-133">Establezca el parámetro _lpulMax_ en el valor mínimo además de la unidad actual multiplicado por la variable establecida en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="695f7-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="695f7-134">Establezca el parámetro _lpulFlags_ en 0.</span><span class="sxs-lookup"><span data-stu-id="695f7-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="695f7-135">Lleve a cabo el procesamiento se debe realizar en este objeto.</span><span class="sxs-lookup"><span data-stu-id="695f7-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="695f7-136">Si el objeto es un subobjetos y su proveedor muestra el progreso de subobjetos, pase un puntero al objeto de progreso en el parámetro _lpProgress_ para el método.</span><span class="sxs-lookup"><span data-stu-id="695f7-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="695f7-137">Llame a [IMAPIProgress::Progress](imapiprogress-progress.md) y pase los siguientes valores para los tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="695f7-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="695f7-138">Establezca el parámetro _ulValue_ a la variable se establece en el paso 2 multiplicado por el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="695f7-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="695f7-139">Establezca el parámetro _ulCount_ en 0.</span><span class="sxs-lookup"><span data-stu-id="695f7-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="695f7-140">Establezca el parámetro _ulTotal_ en 0.</span><span class="sxs-lookup"><span data-stu-id="695f7-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="695f7-141">En el ejemplo de código siguiente se ilustra la lógica necesaria para mostrar el progreso en todos los niveles de una operación que copia el contenido de una carpeta que contiene las cinco subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="695f7-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
```cpp
lpProgress->GetFlags (lpulFlags);
ulFlags = *lpulFlags;
/* The folder in charge of the display. It contains 5 subfolders. */
if (ulFlags & MAPI_TOP_LEVEL)
{
    ulItems = 5                         // 5 subfolders in this folder
    ulScale = (ulMax / ulItems)         // 200 because ulMax = 1000
    lpProgress->SetLimits(0, ulMax, MAPI_TOP_LEVEL)
    for (i = 1; i <= ulItems; i++)      // for each subfolder to copy
    {
        lpProgress->SetLimits( (i - 1) * ulScale, i * ulScale, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        lpProgress->Progress( i * ulScale, i, ulItems)
    }
}
else
/* One of the subfolders to be copied. It contains 3 messages. */
{
    lpProgress->GetMin(&ulMin);
    lpProgress->GetMax(&ulMax);
    ulItems = 3;
    ulDelta = (ulMax - ulMin) / ulItems;
    for (i = 1; i <= ulItems; i++)
    {
        lpProgress->SetLimits(ulMin + (i - 1) * ulDelta,
                              ulMin + i * ulDelta, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        /* Pass 0 for ulCount and ulTotal because this is not the */
        /* top-level display, and that information is unavailable  */
        lpProgress->Progress( i * ulDelta, 0, 0)
    }
}
 
```

## <a name="see-also"></a><span data-ttu-id="695f7-142">Ver también</span><span class="sxs-lookup"><span data-stu-id="695f7-142">See also</span></span>

- [<span data-ttu-id="695f7-143">Indicadores de progreso MAPI</span><span class="sxs-lookup"><span data-stu-id="695f7-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)


---
title: Mostrar un indicador de progreso
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7b0ce0ab75ffdce045ccde5bf6ea8a7da046f463
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345132"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="82ed0-103">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="82ed0-103">Display a progress indicator</span></span>
 
<span data-ttu-id="82ed0-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82ed0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82ed0-105">Para mostrar un indicador de progreso, llame a [método imapiprogress:: GetFlags](imapiprogress-getflags.md) para recuperar la configuración actual de los marcadores.</span><span class="sxs-lookup"><span data-stu-id="82ed0-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="82ed0-106">Si se establece la marca MAPI_TOP_LEVEL, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="82ed0-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="82ed0-107">Establezca una variable igual a la cantidad total de elementos que se van a procesar en la operación.</span><span class="sxs-lookup"><span data-stu-id="82ed0-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="82ed0-108">Por ejemplo, si copia el contenido de una carpeta, este valor será igual al número de las subcarpetas de la carpeta más el número de mensajes.</span><span class="sxs-lookup"><span data-stu-id="82ed0-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="82ed0-109">Establezca una variable igual a 1000 dividida entre el número de elementos.</span><span class="sxs-lookup"><span data-stu-id="82ed0-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="82ed0-110">Si muestra el progreso de los subobjetos, llame al método [método imapiprogress:: SetLimits](imapiprogress-setlimits.md) del objeto Progress y pase los siguientes valores para los tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="82ed0-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="82ed0-111">Establezca el parámetro _lpulMin_ en 0.</span><span class="sxs-lookup"><span data-stu-id="82ed0-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="82ed0-112">Establezca el parámetro _lpulMax_ en 1000.</span><span class="sxs-lookup"><span data-stu-id="82ed0-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="82ed0-113">Establezca el parámetro _lpulFlags_ en MAPI_TOP_LEVEL.</span><span class="sxs-lookup"><span data-stu-id="82ed0-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="82ed0-114">Para cada objeto que se va a procesar, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="82ed0-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="82ed0-115">Llame a **método imapiprogress:: SetLimits** y pase los siguientes valores para los tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="82ed0-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="82ed0-116">Establezca el parámetro _lpulMin_ en el conjunto de variables del paso 2 multiplicado por el elemento actual menos 1.</span><span class="sxs-lookup"><span data-stu-id="82ed0-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="82ed0-117">Establezca el parámetro _lpulMax_ en el conjunto de variables del paso 2 multiplicado por el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="82ed0-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="82ed0-118">Establezca el parámetro _lpulFlags_ en 0.</span><span class="sxs-lookup"><span data-stu-id="82ed0-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="82ed0-119">Realice todo el procesamiento que deba realizarse en este objeto.</span><span class="sxs-lookup"><span data-stu-id="82ed0-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="82ed0-120">Si se trata de un subobjeto y desea mostrar el progreso en los subobjetos, pase al método un puntero al objeto Progress en el parámetro _lpProgress_ .</span><span class="sxs-lookup"><span data-stu-id="82ed0-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="82ed0-121">Llame a [método imapiprogress::P rogress](imapiprogress-progress.md) y pase los siguientes valores para los tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="82ed0-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="82ed0-122">Establezca el parámetro _ulValue_ en el conjunto de variables del paso 2 multiplicado por el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="82ed0-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="82ed0-123">Establezca el parámetro _ulCount_ en el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="82ed0-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="82ed0-124">Establezca el parámetro _ulTotal_ en la variable definida en el paso 1, el número total de objetos.</span><span class="sxs-lookup"><span data-stu-id="82ed0-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="82ed0-125">Si no se establece la marca MAPI_TOP_LEVEL, complete los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="82ed0-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="82ed0-126">Llame al método [método imapiprogress:: GetMin](imapiprogress-getmin.md) del objeto Progress para recuperar el valor mínimo de la presentación.</span><span class="sxs-lookup"><span data-stu-id="82ed0-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="82ed0-127">Llamar a [método imapiprogress:: GetMax](imapiprogress-getmax.md) para recuperar el valor máximo de la presentación.</span><span class="sxs-lookup"><span data-stu-id="82ed0-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="82ed0-128">Establezca una variable igual al número total de objetos que se van a procesar.</span><span class="sxs-lookup"><span data-stu-id="82ed0-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="82ed0-129">Establezca una variable igual al resultado de restar el valor mínimo del valor máximo y, a continuación, dividirlo por el número total de objetos.</span><span class="sxs-lookup"><span data-stu-id="82ed0-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="82ed0-130">Para cada objeto que se va a procesar, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="82ed0-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="82ed0-131">Si su proveedor muestra el progreso de los subobjetos, llame a **método imapiprogress:: SetLimits** y pase los siguientes valores para los tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="82ed0-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="82ed0-132">Establezca el parámetro _lpulMin_ en el valor mínimo más el elemento actual menos 1 multiplicado por la variable definida en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="82ed0-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="82ed0-133">Establezca el parámetro _lpulMax_ en el valor mínimo más la unidad actual multiplicada por la variable definida en el paso 4.</span><span class="sxs-lookup"><span data-stu-id="82ed0-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="82ed0-134">Establezca el parámetro _lpulFlags_ en 0.</span><span class="sxs-lookup"><span data-stu-id="82ed0-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="82ed0-135">Realice todo el procesamiento que deba realizarse en este objeto.</span><span class="sxs-lookup"><span data-stu-id="82ed0-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="82ed0-136">Si el objeto es un subobjeto y el proveedor muestra el progreso de los subobjetos, pase un puntero al objeto Progress en el parámetro _lpProgress_ al método.</span><span class="sxs-lookup"><span data-stu-id="82ed0-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="82ed0-137">Llame a [método imapiprogress::P rogress](imapiprogress-progress.md) y pase los siguientes valores para los tres parámetros:</span><span class="sxs-lookup"><span data-stu-id="82ed0-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="82ed0-138">Establezca el parámetro _ulValue_ en el conjunto de variables en el paso 2 multiplicado por el objeto actual.</span><span class="sxs-lookup"><span data-stu-id="82ed0-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="82ed0-139">Establezca el parámetro _ulCount_ en 0.</span><span class="sxs-lookup"><span data-stu-id="82ed0-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="82ed0-140">Establezca el parámetro _ulTotal_ en 0.</span><span class="sxs-lookup"><span data-stu-id="82ed0-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="82ed0-141">El siguiente ejemplo de código ilustra la lógica necesaria para mostrar el progreso en todos los niveles de una operación que copia el contenido de una carpeta que contiene cinco subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="82ed0-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="82ed0-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="82ed0-142">See also</span></span>

- [<span data-ttu-id="82ed0-143">Indicadores de progreso de MAPI</span><span class="sxs-lookup"><span data-stu-id="82ed0-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)


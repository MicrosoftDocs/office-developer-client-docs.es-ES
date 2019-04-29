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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408030"
---
# <a name="display-a-progress-indicator"></a>Mostrar un indicador de progreso
 
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Para mostrar un indicador de progreso, llame a [método imapiprogress:: GetFlags](imapiprogress-getflags.md) para recuperar la configuración actual de los marcadores. 
  
Si se establece la marca MAPI_TOP_LEVEL, siga estos pasos:
  
1. Establezca una variable igual a la cantidad total de elementos que se van a procesar en la operación. Por ejemplo, si copia el contenido de una carpeta, este valor será igual al número de las subcarpetas de la carpeta más el número de mensajes. 
    
2. Establezca una variable igual a 1000 dividida entre el número de elementos. 
    
3. Si muestra el progreso de los subobjetos, llame al método [método imapiprogress:: SetLimits](imapiprogress-setlimits.md) del objeto Progress y pase los siguientes valores para los tres parámetros: 
    
   - Establezca el parámetro _lpulMin_ en 0. 
    
   - Establezca el parámetro _lpulMax_ en 1000. 
    
   - Establezca el parámetro _lpulFlags_ en MAPI_TOP_LEVEL. 
    
4. Para cada objeto que se va a procesar, siga estos pasos:
    
   1. Llame a **método imapiprogress:: SetLimits** y pase los siguientes valores para los tres parámetros: 
      
     - Establezca el parámetro _lpulMin_ en el conjunto de variables del paso 2 multiplicado por el elemento actual menos 1. 
      
     - Establezca el parámetro _lpulMax_ en el conjunto de variables del paso 2 multiplicado por el objeto actual. 
      
     - Establezca el parámetro _lpulFlags_ en 0. 
      
   2. Realice todo el procesamiento que deba realizarse en este objeto. Si se trata de un subobjeto y desea mostrar el progreso en los subobjetos, pase al método un puntero al objeto Progress en el parámetro _lpProgress_ . 
      
   3. Llame a [método imapiprogress::P rogress](imapiprogress-progress.md) y pase los siguientes valores para los tres parámetros: 
      
     - Establezca el parámetro _ulValue_ en el conjunto de variables del paso 2 multiplicado por el objeto actual. 
      
     - Establezca el parámetro _ulCount_ en el objeto actual. 
      
     - Establezca el parámetro _ulTotal_ en la variable definida en el paso 1, el número total de objetos. 
    
Si no se establece la marca MAPI_TOP_LEVEL, complete los siguientes pasos:
  
1. Llame al método [método imapiprogress:: GetMin](imapiprogress-getmin.md) del objeto Progress para recuperar el valor mínimo de la presentación. 
    
2. Llamar a [método imapiprogress:: GetMax](imapiprogress-getmax.md) para recuperar el valor máximo de la presentación. 
    
3. Establezca una variable igual al número total de objetos que se van a procesar. 
    
4. Establezca una variable igual al resultado de restar el valor mínimo del valor máximo y, a continuación, dividirlo por el número total de objetos.
    
5. Para cada objeto que se va a procesar, siga estos pasos:
    
   1. Si su proveedor muestra el progreso de los subobjetos, llame a **método imapiprogress:: SetLimits** y pase los siguientes valores para los tres parámetros: 
      
     - Establezca el parámetro _lpulMin_ en el valor mínimo más el elemento actual menos 1 multiplicado por la variable definida en el paso 4. 
      
     - Establezca el parámetro _lpulMax_ en el valor mínimo más la unidad actual multiplicada por la variable definida en el paso 4. 
      
     - Establezca el parámetro _lpulFlags_ en 0. 
      
   2. Realice todo el procesamiento que deba realizarse en este objeto. Si el objeto es un subobjeto y el proveedor muestra el progreso de los subobjetos, pase un puntero al objeto Progress en el parámetro _lpProgress_ al método. 
      
   3. Llame a [método imapiprogress::P rogress](imapiprogress-progress.md) y pase los siguientes valores para los tres parámetros: 
      
     - Establezca el parámetro _ulValue_ en el conjunto de variables en el paso 2 multiplicado por el objeto actual. 
      
     - Establezca el parámetro _ulCount_ en 0. 
      
     - Establezca el parámetro _ulTotal_ en 0. 
    
El siguiente ejemplo de código ilustra la lógica necesaria para mostrar el progreso en todos los niveles de una operación que copia el contenido de una carpeta que contiene cinco subcarpetas. 
  
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

## <a name="see-also"></a>Ver también

- [Indicadores de progreso de MAPI](mapi-progress-indicators.md)


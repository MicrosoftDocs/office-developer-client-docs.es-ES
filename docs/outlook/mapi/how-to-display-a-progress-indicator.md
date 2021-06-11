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
  
Para mostrar un indicador de progreso, llama [a IMAPIProgress::GetFlags](imapiprogress-getflags.md) para recuperar la configuración de marcas actual. 
  
Si se MAPI_TOP_LEVEL marca, siga estos pasos:
  
1. Establezca una variable igual al número total de elementos que se procesarán en la operación. Por ejemplo, si va a copiar el contenido de una carpeta, este valor será igual al número de subcarpetas de la carpeta más el número de mensajes. 
    
2. Establezca una variable igual a 1000 dividida por el número de elementos. 
    
3. Si va a mostrar el progreso de los subobjetos, llame al método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) del objeto de progreso y pase los siguientes valores para los tres parámetros: 
    
   - Establezca el  _parámetro lpulMin_ en 0. 
    
   - Establezca el  _parámetro lpulMax_ en 1000. 
    
   - Establezca el  _parámetro lpulFlags_ en MAPI_TOP_LEVEL. 
    
4. Para cada objeto que se va a procesar, siga estos pasos:
    
   1. Llama **a IMAPIProgress::SetLimits** y pasa los siguientes valores para los tres parámetros: 
      
     - Establezca el  _parámetro lpulMin_ en la variable establecida en el paso 2 multiplicado por el elemento actual menos 1. 
      
     - Establezca el  _parámetro lpulMax_ en la variable establecida en el paso 2 multiplicado por el objeto actual. 
      
     - Establezca el  _parámetro lpulFlags_ en 0. 
      
   2. Realice cualquier procesamiento que se debe realizar en este objeto. Si se trata de un subobjeto y desea mostrar el progreso de los subobjetos, pase un puntero al objeto progress en el parámetro  _lpProgress_ al método. 
      
   3. Llama [a IMAPIProgress::P rogress](imapiprogress-progress.md) y pasa los siguientes valores para los tres parámetros: 
      
     - Establezca el  _parámetro ulValue_ en la variable establecida en el paso 2 multiplicado por el objeto actual. 
      
     - Establezca el  _parámetro ulCount_ en el objeto actual. 
      
     - Establezca el  _parámetro ulTotal_ en la variable establecida en el paso 1, el número total de objetos. 
    
Si la MAPI_TOP_LEVEL no está establecida, siga estos pasos:
  
1. Llame al método [IMAPIProgress::GetMin](imapiprogress-getmin.md) del objeto de progreso para recuperar el valor mínimo para la presentación. 
    
2. Llama [a IMAPIProgress::GetMax](imapiprogress-getmax.md) para recuperar el valor máximo de la pantalla. 
    
3. Establezca una variable igual al número total de objetos que se procesarán. 
    
4. Establezca una variable igual al resultado de restar el valor mínimo del valor máximo y, a continuación, dividir por el número total de objetos.
    
5. Para cada objeto que se va a procesar, siga estos pasos:
    
   1. Si el proveedor muestra el progreso de los subobjetos, llame a **IMAPIProgress::SetLimits** y pase los siguientes valores para los tres parámetros: 
      
     - Establezca el  _parámetro lpulMin_ en el valor mínimo más el elemento actual menos 1 multiplicado por la variable establecida en el paso 4. 
      
     - Establezca el  _parámetro lpulMax_ en el valor mínimo más la unidad actual multiplicada por la variable establecida en el paso 4. 
      
     - Establezca el  _parámetro lpulFlags_ en 0. 
      
   2. Realice cualquier procesamiento que se debe realizar en este objeto. Si el objeto es un subobjeto y el proveedor muestra el progreso de los subobjetos, pase un puntero al objeto de progreso en el parámetro  _lpProgress_ al método. 
      
   3. Llama [a IMAPIProgress::P rogress](imapiprogress-progress.md) y pasa los siguientes valores para los tres parámetros: 
      
     - Establezca el  _parámetro ulValue_ en variable establecida en el paso 2 multiplicado por el objeto actual. 
      
     - Establezca el  _parámetro ulCount_ en 0. 
      
     - Establezca el  _parámetro ulTotal_ en 0. 
    
En el siguiente ejemplo de código se muestra la lógica necesaria para mostrar el progreso en todos los niveles de una operación que copia el contenido de una carpeta que contiene cinco subcarpetas. 
  
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

## <a name="see-also"></a>Vea también

- [Indicadores de progreso mapi](mapi-progress-indicators.md)


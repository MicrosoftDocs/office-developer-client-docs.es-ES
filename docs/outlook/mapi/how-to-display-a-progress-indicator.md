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
# <a name="display-a-progress-indicator"></a>Mostrar un indicador de progreso
 
**Se aplica a**: Outlook 
  
Para mostrar un indicador de progreso, llame a [IMAPIProgress::GetFlags](imapiprogress-getflags.md) para recuperar los indicadores actuales de configuración. 
  
Si se establece la marca MAPI_TOP_LEVEL, complete los siguientes pasos:
  
1. Establezca a una variable igual al número total de elementos que se procesan en la operación. Por ejemplo, si va a copiar el contenido de una carpeta, este valor será igual que el número de las subcarpetas de la carpeta más el número de mensajes. 
    
2. Establezca a una variable igual a 1000 dividido por el número de elementos. 
    
3. Si se muestra el progreso de subobjetos, llamar al método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) del objeto de progreso y pasar los siguientes valores para los tres parámetros: 
    
   - Establezca el parámetro _lpulMin_ en 0. 
    
   - Establezca el parámetro _lpulMax_ en 1000. 
    
   - Establezca el parámetro _lpulFlags_ en MAPI_TOP_LEVEL. 
    
4. Para que cada objeto que va a procesar, complete los siguientes pasos:
    
   1. Llame a **IMAPIProgress::SetLimits** y pase los siguientes valores para los tres parámetros: 
      
     - Establezca el parámetro _lpulMin_ en la variable establecida en el paso 2 multiplicado por el elemento actual menos 1. 
      
     - Establezca el parámetro _lpulMax_ en la variable establecida en el paso 2 multiplicado por el objeto actual. 
      
     - Establezca el parámetro _lpulFlags_ en 0. 
      
   2. Lleve a cabo el procesamiento se debe realizar en este objeto. Si se trata de un subobjetos y desea mostrar el progreso en subobjetos, pase un puntero al objeto de progreso en el parámetro _lpProgress_ para el método. 
      
   3. Llame a [IMAPIProgress::Progress](imapiprogress-progress.md) y pase los siguientes valores para los tres parámetros: 
      
     - Establezca el parámetro _ulValue_ en la variable establecida en el paso 2 multiplicado por el objeto actual. 
      
     - Establezca el parámetro _ulCount_ en el objeto actual. 
      
     - Establezca el parámetro _ulTotal_ en la variable establecida en el paso 1, el número total de objetos. 
    
Si no está establecido el indicador MAPI_TOP_LEVEL, complete los pasos siguientes:
  
1. Llamar al método [IMAPIProgress::GetMin](imapiprogress-getmin.md) del objeto de progreso para recuperar el valor mínimo para la presentación. 
    
2. Llame a [IMAPIProgress::GetMax](imapiprogress-getmax.md) para recuperar el valor máximo para la presentación. 
    
3. Establezca a una variable igual al número total de objetos que va a procesar. 
    
4. Establezca a una variable igual al resultado de restar el valor mínimo del valor máximo y, a continuación, dividiendo el número total de objetos.
    
5. Para que cada objeto que va a procesar, complete los siguientes pasos:
    
   1. Si su proveedor es que muestra el progreso de subobjetos, llamar **IMAPIProgress::SetLimits** y pasar los siguientes valores para los tres parámetros: 
      
     - Establezca el parámetro _lpulMin_ en el valor mínimo más el elemento actual menos 1 multiplicado por la variable establecida en el paso 4. 
      
     - Establezca el parámetro _lpulMax_ en el valor mínimo además de la unidad actual multiplicado por la variable establecida en el paso 4. 
      
     - Establezca el parámetro _lpulFlags_ en 0. 
      
   2. Lleve a cabo el procesamiento se debe realizar en este objeto. Si el objeto es un subobjetos y su proveedor muestra el progreso de subobjetos, pase un puntero al objeto de progreso en el parámetro _lpProgress_ para el método. 
      
   3. Llame a [IMAPIProgress::Progress](imapiprogress-progress.md) y pase los siguientes valores para los tres parámetros: 
      
     - Establezca el parámetro _ulValue_ a la variable se establece en el paso 2 multiplicado por el objeto actual. 
      
     - Establezca el parámetro _ulCount_ en 0. 
      
     - Establezca el parámetro _ulTotal_ en 0. 
    
En el ejemplo de código siguiente se ilustra la lógica necesaria para mostrar el progreso en todos los niveles de una operación que copia el contenido de una carpeta que contiene las cinco subcarpetas. 
  
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

- [Indicadores de progreso MAPI](mapi-progress-indicators.md)


---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421469"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece los límites inferior y superior para el número de elementos de la operación y las marcas que controlan cómo se calcula la información de progreso de la operación.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpulMin_
  
> a Un puntero a una variable que contiene el límite inferior de los elementos de la operación.
    
 _lpulMax_
  
> a Un puntero a una variable que contiene el límite superior de los elementos de la operación.
    
 _lpulFlags_
  
> a Máscara de máscara de marcadores que controla el nivel de funcionamiento en el que se calcula la información del progreso. Se puede establecer la siguiente marca:
    
MAPI_TOP_LEVEL 
  
> Utiliza los valores de los parámetros _ulCount_ y _UlTotal_ del método [método imapiprogress::P rogress](imapiprogress-progress.md) , que indican el elemento actualmente procesado y los elementos totales, respectivamente, para incrementar el progreso de la operación. Cuando se establece este indicador, se deben establecer los valores de los límites inferior y superior globales. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Los proveedores de servicios llaman al método **método imapiprogress:: SetLimits** para establecer o borrar la marca MAPI_TOP_LEVEL y para establecer valores mínimos y máximos locales y globales. El valor de la configuración de la marca determina si el objeto Progress comprende los valores mínimos y máximos locales o globales. Cuando se establece la marca MAPI_TOP_LEVEL, estos valores se consideran globales y se usan para calcular el progreso de toda la operación. Los objetos de progreso inicializan el valor mínimo global en 1 y el valor máximo global en 1000. 
  
Cuando MAPI_TOP_LEVEL no se establece, los valores mínimos y máximos se consideran locales y los proveedores los usan internamente para mostrar el progreso de los subobjetos de nivel inferior. Los objetos de progreso guardan los valores mínimos y máximos locales solo para que se puedan devolver a los proveedores cuando se llama a los métodos [método imapiprogress:: GetMin](imapiprogress-getmin.md) y [método imapiprogress:: GetMax](imapiprogress-getmax.md) . 
  
Para obtener más información sobre cómo implementar **SetLimits** y los otros métodos de [método imapiprogress](imapiprogressiunknown.md) , consulte [implementación de un indicador de progreso](implementing-a-progress-indicator.md).
  
Para obtener más información sobre cómo y cuándo debe realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress:: SetLimits  <br/> |MFCMAPI usa el método **método imapiprogress:: SetLimits** para establecer los límites máximos y mínimos y los marcadores del objeto Progress.  <br/> |
   
## <a name="see-also"></a>Vea también



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como un ejemplo de código](mfcmapi-as-a-code-sample.md)
  
[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)
  
[Implementar un indicador de progreso](implementing-a-progress-indicator.md)


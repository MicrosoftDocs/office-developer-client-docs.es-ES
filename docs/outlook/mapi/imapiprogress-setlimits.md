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
ms.openlocfilehash: 010f69b70324d4280a34d2fe06d670e07d922d86
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586777"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece los límites superiores e inferiores para el número de elementos de la operación y los indicadores que controlan cómo se calcula la información de progreso de la operación.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Parámetros

 _lpulMin_
  
> [entrada] Un puntero a una variable que contiene el límite inferior de los elementos de la operación.
    
 _lpulMax_
  
> [entrada] Un puntero a una variable que contenga el límite superior de los elementos de la operación.
    
 _lpulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla el nivel de operación en progreso que se calcula de la información. Se puede establecer la marca siguiente:
    
MAPI_TOP_LEVEL 
  
> Utiliza los valores de parámetros del método [IMAPIProgress::Progress](imapiprogress-progress.md) _ulCount_ y _ulTotal_ que indican el elemento procesado actualmente y los elementos totales, respectivamente, para incremento del progreso de la operación. Cuando se establece este marcador, los valores de los límites superiores e inferiores global tienen que establecerse. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Proveedores de servicios de llamar al método **IMAPIProgress::SetLimits** para establecer o borrar la marca MAPI_TOP_LEVEL y para establecer los valores máximos y mínimos locales y global. El valor de la opción marca determina si el objeto de progreso comprende los valores máximos y mínimos para ser local o global. Cuando se establece la marca MAPI_TOP_LEVEL, estos valores se consideran global y se usan para calcular el progreso de toda la operación. Objetos de progreso inicialización el valor mínimo global a 1 y el valor máximo global a 1000. 
  
Cuando MAPI_TOP_LEVEL no está establecida, los valores máximos y mínimos se consideran locales, y que los proveedores de use internamente para mostrar progreso para subobjetos de nivel inferiores. Objetos de progreso guardan los valores máximos y mínimos locales sólo por lo que puede devolverse a proveedores cuando se llaman a los métodos [IMAPIProgress::GetMin](imapiprogress-getmin.md) y [IMAPIProgress::GetMax](imapiprogress-getmax.md) . 
  
Para obtener más información acerca de cómo implementar otros métodos [IMAPIProgress](imapiprogressiunknown.md) y **SetLimits** , vea [implementar un indicador de progreso](implementing-a-progress-indicator.md).
  
Para que obtener más información acerca de cómo y cuándo se deben realizar llamadas a un objeto de progreso, vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI usa el método **IMAPIProgress::SetLimits** para establecer los límites máximos y mínimos y los indicadores para el objeto de progreso.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)
  
[Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md)
  
[Implementar un indicador de progreso](implementing-a-progress-indicator.md)

